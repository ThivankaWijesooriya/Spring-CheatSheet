package com.ONEzero.DAO;

import java.util.ArrayList;
import java.util.List;

import com.ONEzero.model.Department;
import com.ONEzero.model.Designation;

import com.ONEzero.service.DBUtil2;
import com.google.gson.Gson;

import java.sql.*;

public class DepartmentDAOImpl implements DepartmentDAO {

	@Override
	public void createDepartment(Department department) {
		
		
		/*String sql = "INSERT INTO tblRefDepartment (strDeptID,strDeptName,intStatus,strRemarks,strEnteredBy,dtmEnteredDate) VALUES (?,?,?,?,?,GETDATE())";*/
		
		String sql ="{call spInsertDepartment(?,?,?,?)}";  
		
		try(Connection con = DBUtil2.getInstance().getConnection();CallableStatement stmt = con.prepareCall(sql)) {
			
			
			
			stmt.setString(1, department.getDeptname());
			stmt.setInt(2, department.getStatus());
			stmt.setString(3, department.getRemarks());
			stmt.setString(4, department.getEnteredby()); 
			
			/*stmt.setString(4, "Thivanka"); */ // UNDO during Initial Config
			
			
			int result = stmt.executeUpdate();
			
			if(result==1) {
				
				System.out.println("Record Created");
				
			}
			
			else {
				
				System.out.println("Record Not Created");
			}
			
			
		} catch (Exception e) {
			
			e.printStackTrace();
			
		}

	}
	
	

	@Override
	public String getAllDepartments() {

		/*String sql = "SELECT * from tblRefDepartment WHERE intStatus != 2";*/
		String sql ="{call spGetAllDepartments}";  		
		String StringDeptlist=null;
		List<Department> deptlist = new ArrayList<Department>();
		

		try(Connection con = DBUtil2.getInstance().getConnection();CallableStatement stmt = con.prepareCall(sql)) {

			
			try(ResultSet rs = stmt.executeQuery()) {
				
				if(rs.next()==false) {
					
					Department dept = new Department("","","","");
	   			    deptlist.add(dept);
					
					
				}
				
				else {
					
					do {
						
					
			               if(rs.getInt("intStatus")==1) {
						    	
						    	String state = "Active";
						    	
						    	 Department dept = new Department(rs.getString("strDeptCode"),rs.getString("strDeptName"),state,rs.getString("strRemarks"));
				    			 deptlist.add(dept);
						    	
						    }
						    
						    else if(rs.getInt("intStatus")==0){
						    	
						    	String state = "Inactive";
						    	
						    	 Department dept = new Department(rs.getString("strDeptCode"),rs.getString("strDeptName"),state,rs.getString("strRemarks"));
				    			 deptlist.add(dept);
						    }
						    
						    else {
						    	
						    	
			                    String state = "Deleted";
						    	
			                    Department dept = new Department(rs.getString("strDeptCode"),rs.getString("strDeptName"),state,rs.getString("strRemarks"));
			    				deptlist.add(dept);
						    	
						    	
						    }
						
						
						
					}while(rs.next());
					
					
				}
				
				
			} catch (Exception e) {
				
				e.printStackTrace();
			}
			

			
			Gson gson = new Gson();
			StringDeptlist = gson.toJson(deptlist);
			


		} catch (Exception e) {

			e.printStackTrace();

		}
		
		

		return StringDeptlist;

	}
	
	

	@Override
	public void updateDepartmentById(Department department) {
		
		
		String sql = "UPDATE tblRefDepartment SET strDeptName = ?, intStatus = ?, strRemarks = ? , strUpdatedBy = ? , dtmUpdatedDate = GETDATE() "
				+ "WHERE strDeptCode = ? AND (strUpdatedBy is null OR strUpdatedBy IS NOT null) AND (dtmUpdatedDate is null OR dtmUpdatedDate IS NOT null)";
		
		try(Connection con = DBUtil2.getInstance().getConnection();PreparedStatement stmt = con.prepareStatement(sql)) {

			
			stmt.setString(1, department.getDeptname());
			stmt.setInt(2, department.getStatus());
			stmt.setString(3, department.getRemarks());
			stmt.setString(4, department.getUpdatedby());
			stmt.setString(5, department.getDeptid());
			
			int result = stmt.executeUpdate();
			
			if(result==1) {
				
				System.out.println("Record Updated");
			}
			
			else {
				
				System.out.println("Record Not Updated");
				
			}
			
		} catch (Exception e) {
			
			e.printStackTrace();
			
		}
		

	}
	
	

	@Override
	public void deleteDepartmentById(Department department) {
		
		
		String sql = "UPDATE tblRefDepartment SET intStatus = ? , strDeletedBy = ? , dtmDeletedDate = GETDATE()"
				+ " WHERE strDeptCode = ? AND (strDeletedBy is null OR strDeletedBy IS NOT null) AND (dtmDeletedDate is null OR dtmDeletedDate IS NOT null)";
		
		try(Connection con = DBUtil2.getInstance().getConnection();PreparedStatement stmt = con.prepareStatement(sql)) {
			
			
			stmt.setInt(1, department.getStatus());
			stmt.setString(2, department.getDeletedby());
			stmt.setString(3, department.getDeptid());
			
			int result = stmt.executeUpdate();
			
			if(result==1) {
				
				System.out.println("Record Deleted");
			}
			
			else {
				
				System.out.println("Record Not Deleted");
				
			}
			
		} catch (Exception e) {
			
			e.printStackTrace();
			
		}

	}



	@Override
	public String getDepartmentsToEmployeeMast() {
		
		/*String sql = "SELECT * from tblRefDepartment WHERE intStatus != 2";*/
		String sql ="{call spGetDepartmentsToEmployeeMast}";  
		List<Department> deptlist = new ArrayList<Department>(); 
		String StringDeptlist=null;
		

		try(Connection con = DBUtil2.getInstance().getConnection();CallableStatement stmt = con.prepareCall(sql)) {
			
			
			try (ResultSet rs = stmt.executeQuery()){
				
				while(rs.next()) {
					
					
		               if(rs.getInt("intStatus")==1) {
					    	
					    	String state = "Active";
					    	
					    	 Department dept = new Department(rs.getString("strDeptCode"),rs.getString("strDeptName"),state,rs.getString("strRemarks"));
			    			 deptlist.add(dept);
					    	
					    }
					    
					    else if(rs.getInt("intStatus")==0){
					    	
					    	String state = "Inactive";
					    	
					    	 Department dept = new Department(rs.getString("strDeptCode"),rs.getString("strDeptName"),state,rs.getString("strRemarks"));
			    			 deptlist.add(dept);
					    }
					    
					    else {
					    	
					    	
		                    String state = "Deleted";
					    	
		                    Department dept = new Department(rs.getString("strDeptCode"),rs.getString("strDeptName"),state,rs.getString("strRemarks"));
		    				deptlist.add(dept);
					    	
					    	
					    }
									
						
					}
				
			} catch (Exception e) {
				
			  e.printStackTrace();
			  
			}
			
			Gson gson = new Gson();
			StringDeptlist = gson.toJson(deptlist);
			


		} catch (Exception e) {

			e.printStackTrace();

		}
		
		

		return StringDeptlist;
			
		
	}



	@Override
	public String getDepartmentsByName(String deptname) {
		
		
		String sql = "{call getDeptByName(?)}";
		List<Department> deptlist = new ArrayList<>();
		String strdeptlist = null;
		
		try(Connection con  = DBUtil2.getInstance().getConnection();CallableStatement stmt = con.prepareCall(sql)) {
			
			if(deptname == null) {
				
				
				deptname = "";
				stmt.setString(1, deptname);
				
			}
			
			else {
				
				stmt.setString(1, deptname);
				
			}
			
			try(ResultSet rs = stmt.executeQuery()) {
				
				while(rs.next()) {
					
					Department deptobj = new Department(rs.getString("strDeptCode"),rs.getString("strDeptName"));
					deptlist.add(deptobj);
				}
				
			} catch (Exception e) {
				
				e.printStackTrace();
			}
			
			Gson gson = new Gson();
			strdeptlist = gson.toJson(deptlist);
			
			
		} catch (Exception e) {
			
			e.printStackTrace();
		}
		
		
		return strdeptlist;
		
	}

}
