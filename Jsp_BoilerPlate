<%@taglib prefix="c" uri="http://java.sun.com/jsp/jstl/core"%>
<%@taglib prefix="form" uri="http://www.springframework.org/tags/form"%>
<%@taglib uri="http://www.springframework.org/security/tags" prefix="sec" %>

<!DOCTYPE html>
<html lang="en">

<head>

<meta charset="utf-8">
<meta http-equiv="X-UA-Compatible" content="IE=edge">
<meta name="viewport" content="width=device-width, initial-scale=1">
<meta name="description" content="">
<meta name="author" content="">

<title>ONEzero Petty Cash Management</title>

<!-- Bootstrap Core CSS -->

<link href="<c:url value="/resources/css/bootstrap.min.css" />"
	rel="stylesheet" />


<!-- Custom CSS -->
<link href="<c:url value="/resources/css/sb-admin.css" />"
	rel="stylesheet" />
<link href="<c:url value="/resources/css/custom.css" />"
	rel="stylesheet" />

<!-- Custom Fonts -->
<link
	href="<c:url value="/resources/font-awesome/css/font-awesome.min.css" />"
	rel="stylesheet" />

<link
	href="<c:url value="/resources/css/datatables.min.css" />"
	rel="stylesheet" />

<style type="text/css">
.error {
	color: red;
}
</style>

</head>

<body>

<div id="wrapper">

<%@ include file ="../common/navbar.jspf" %>

		<div id="page-wrapper">

			<div class="container-fluid nopaddingarea">

				<!-- Page Heading -->
				<div class="row">
					<div class="col-lg-12">
						<h1 class="page-header">
							Employee Master
						</h1>
						

						<div class="panel panel-warning">
							
							<div class="panel-body">

								<form:form id="employeeform"
									action="${pageContext.request.contextPath}/Employee/Submit?${_csrf.parameterName}=${_csrf.token}"
									method="POST" modelAttribute="Employee"
									enctype="multipart/form-data">



									<div class="col-md-6">

										<div class="form-group">
											<div class="row">
												<!-- <label class="col-sm-3" for="exampleInputEmail1">User
													ID</label> -->
												<div class="col-sm-7">
												
													<input class="form-control" type = "hidden" placeholder="" id="userid"/>
														 
													
												</div>
											</div>
										</div>


										<div class="form-group">
											<div class="row">
												<label class="col-sm-3" for="exampleInputEmail1">Employee
													No. <span class="required">&nbsp; *</span> </label>
												<div class="col-sm-7">
													<form:input class="form-control" placeholder=""
														path="employeeNo" autocomplete="off" maxlength="30"/>
													<form:errors path="employeeNo" cssClass="error" />
												</div>
											</div>
										</div>


										<div class="form-group">
											<div class="row">
												<label class="col-sm-3" for="exampleInputEmail1">Upload
													File</label>
												<div class="col-sm-7">
													<form:input placeholder="" path="multiimage" type="file" value="" />
													<form:errors path="multiimage" cssClass="error" />
													
												</div>
											</div>
										</div>




										<div class="form-group">
											<div class="row">
												<label class="col-sm-3" for="exampleInputEmail1">Emp.
													First Name <span class="required">&nbsp; *</span> </label>
												<div class="col-sm-7">
													<form:input class="form-control" placeholder=""
														path="empfirstname" id="firstname" maxlength="30"/>
													<form:errors path="empfirstname" cssClass="error" />
												</div>
											</div>
										</div>


										<div class="form-group">
											<div class="row">
												<label class="col-sm-3" for="exampleInputEmail1">Emp.
													Last Name <span class="required">&nbsp; *</span> </label>
												<div class="col-sm-7">
													<form:input class="form-control" placeholder=""
														path="emplastname" maxlength="30"/>
													<form:errors path="emplastname" cssClass="error" />
												</div>
											</div>
										</div>


										<div class="form-group">
											<div class="row">
												<label class="col-sm-3" for="exampleInputEmail1">Emp.
													Full Name with Initials <span class="required">&nbsp; *</span></label>
												<div class="col-sm-7">
													<form:input class="form-control" placeholder=""
														path="empfullname" autocomplete="off" maxlength="100"/>
													<form:errors path="empfullname" cssClass="error" />
												</div>
											</div>
										</div>
										
										
										<div class="form-group">
											<div class="row">
												<label class="col-sm-3" for="exampleInputEmail1">Employee
													Type <span class="required">&nbsp; *</span> </label>
												<div class="col-sm-7">

													<form:select path="employeetype" class="form-control">
														<form:option value="" label="--- Select ---" />
														<form:options items="${EmpListType}" />
													</form:select>

													<form:errors path="employeetype" cssClass="error" />

												</div>
											</div>
										</div>
										
										
										<div class="form-group">
											<div class="row">
												<label class="col-sm-3" for="exampleInputEmail1">
													Sex <span class="required">&nbsp; *</span> </label>
												<div class="col-sm-7">

													<form:select path="empsex" class="form-control">
														<form:option value="" label="--- Select ---" />
														<form:option value="M" label="Male" />
														<form:option value="F" label="Female" />

													</form:select>
													<form:errors path="empsex" cssClass="error" />

												</div>

											</div>
										</div>


										<div class="form-group">
											<div class="row">
												<label class="col-sm-3" for="exampleInputEmail1">
													Marital Status <span class="required">&nbsp; *</span> </label>
												<div class="col-sm-7">

													<form:select path="empMaritalStatus" class="form-control">
														<form:option value="" label="--- Select ---" />
														<form:option value="S" label="Single" />
														<form:option value="M" label="Married" />


													</form:select>
													<form:errors path="empMaritalStatus" cssClass="error" />

												</div>

											</div>
										</div>


										<%-- <div class="form-group">
											<div class="row">
												<label class="col-sm-3" for="exampleInputEmail1">Shift <span class="required">&nbsp *</span></label>
												<div class="col-sm-7">
												
												<form:input class="form-control" placeholder="" id="tempshift" path="tempshiftname" />
													<form:input class="form-control" placeholder=""
														path="shift.shiftid" id="shiftfield" type="hidden"/>
														
													<form:errors path="shift.shiftid" cssClass="error" />
												</div>
												<a class="help-btn" href="#" id="shiftbtn"></a>
											</div>
										</div> --%>


										<div class="form-group">
											<div class="row">
												<label class="col-sm-3" for="exampleInputEmail1">Department <span class="required">&nbsp; *</span> </label>
												<div class="col-sm-7">
												
												<form:input class="form-control" placeholder="" id="tempdept" path="tempdeptname" />
												
													<form:input class="form-control" placeholder=""
														path="department.deptid" id="deptfield" type="hidden"/>
													<form:errors path="department.deptid" cssClass="error" />
												</div>
												<a class="help-btn" href="#" id="deptbtn"></a>
											</div>
										</div>


										<div class="form-group">
											<div class="row">
												<label class="col-sm-3" for="exampleInputEmail1">Designation <span class="required">&nbsp; *</span></label>
												<div class="col-sm-7">
												
												<form:input class="form-control" placeholder="" id="tempdesig" path="tempdesigname" />
													<form:input class="form-control" placeholder=""
														path="designation.desigid" id="desigfield" type="hidden"/>
													<form:errors path="designation.desigid" cssClass="error" />
												</div>
												<a class="help-btn" href="#" id="desigbtn"></a>
											</div>
										</div>


										<div class="form-group">
											<div class="row">
												<label class="col-sm-3" for="exampleInputEmail1">Mobile
												</label>
												<div class="col-sm-7">
													<form:input class="form-control" placeholder=""
														path="empmobile" maxlength="10" autocomplete="off"/>
													<form:errors path="empmobile" cssClass="error" />
												</div>
											</div>
										</div>


										<div class="form-group">
											<div class="row">
												<label class="col-sm-3" for="exampleInputEmail1">Telephone
												</label>
												<div class="col-sm-7">
													<form:input class="form-control" placeholder=""
														path="emptp" maxlength="10" autocomplete="off"/>
													<form:errors path="emptp" cssClass="error" />
												</div>
											</div>
										</div>


										<div class="form-group">
											<div class="row">
												<label class="col-sm-3" for="exampleInputEmail1">Email<span class="required">&nbsp; *</span></label>
												<div class="col-sm-7">
													<form:input class="form-control" placeholder=""
														path="email" maxlength="50"/>
													<form:errors path="email" cssClass="error" />
												</div>
											</div>
										</div>







									</div>


									<div class="col-md-6">


										<div class="form-group">
											<div class="row">
												<label class="col-sm-3" for="exampleInputEmail1">Permanent
													Address1 <span class="required">&nbsp; *</span></label>
												<div class="col-sm-7">
													<form:input class="form-control" placeholder=""
														path="pAddress1" maxlength="80"/>
													<form:errors path="pAddress1" cssClass="error" />
												</div>
											</div>
										</div>


										<div class="form-group">
											<div class="row">
												<label class="col-sm-3" for="exampleInputEmail1">Permanent
													Address2 <span class="required">&nbsp; *</span></label>
												<div class="col-sm-7">
													<form:input class="form-control" placeholder=""
														path="pAddress2" maxlength="80"/>
													<form:errors path="pAddress2" cssClass="error" />
												</div>
											</div>
										</div>


										<div class="form-group">
											<div class="row">
												<label class="col-sm-3" for="exampleInputEmail1">Permanent
													Address3 </label>
												<div class="col-sm-7">
													<form:input class="form-control" placeholder=""
														path="pAddress3" maxlength="80"/>
													<form:errors path="pAddress3" cssClass="error" />
												</div>
											</div>
										</div>


										<div class="form-group">
											<div class="row">
												<label class="col-sm-3" for="exampleInputEmail1">Temp
													Address1 </label>
												<div class="col-sm-7">
													<form:input class="form-control" placeholder=""
														path="tAddress1" maxlength="80"/>
													<form:errors path="tAddress1" cssClass="error" />
												</div>
											</div>
										</div>

										<div class="form-group">
											<div class="row">
												<label class="col-sm-3" for="exampleInputEmail1">Temp
													Address2 </label>
												<div class="col-sm-7">
													<form:input class="form-control" placeholder=""
														path="tAddress2" maxlength="80"/>
													<form:errors path="tAddress2" cssClass="error" />
												</div>
											</div>
										</div>


										<div class="form-group">
											<div class="row">
												<label class="col-sm-3" for="exampleInputEmail1">Temp
													Address3 </label>
												<div class="col-sm-7">
													<form:input class="form-control" placeholder=""
														path="tAddress3" maxlength="80"/>
													<form:errors path="tAddress3" cssClass="error" />
												</div>
											</div>
										</div>





										<div class="form-group">
											<div class="row">
												<label class="col-sm-3" for="exampleInputEmail1">Status
												</label>
												<div class="col-sm-7">

													<select disabled class="form-control">
													
													   <option value="1"> Active </option>
													   
													</select>
													
													
													<form:input class="form-control" placeholder=""
													 path="status" value="1" type="hidden"/>
													<form:errors path="status" cssClass="error" />


												</div>
											</div>
										</div>



										<div class="form-group">
											<div class="row">

												<label class="col-sm-3">Is Reporting Officer <span class="required">&nbsp; *</span> </label>
												<div class="checkbox col-sm-7">
													<label> <form:checkbox path="isreportingoff"
															value="" /> Yes <form:errors path="isreportingoff"
															cssClass="error" />

													</label>
												</div>

											</div>
										</div>


										 <div class="form-group">
											<div class="row">
												<label class="col-sm-3" for="exampleInputEmail1">Reporting
													Officer <span class="required">&nbsp; *</span> </label>
												<div class="col-sm-7">
												
												<form:input class="form-control" placeholder="" id="temprptoff1" path="temprptoff1" />
													<form:input class="form-control" placeholder=""
														path="rptoffid" type="hidden"/>
													<form:errors path="rptoffid" cssClass="error" />
												</div>
												<a class="help-btn" href="#" id="rptoffbtn1"></a>
											</div>
										</div> 


										 <div class="form-group">
											<div class="row">
												<label class="col-sm-3" for="exampleInputEmail1">Alt.
													Reporting Officer</label>
												<div class="col-sm-7">
												
												<form:input class="form-control" placeholder="" id="temprptoff2" path="temprptoff2" />
													<form:input class="form-control" placeholder=""
														path="altoffid" type="hidden"/>
													<form:errors path="altoffid" cssClass="error" />
												</div>
												<a class="help-btn" href="#" id="rptoffbtn2"></a>
											</div>
										</div> 


										<div class="form-group">
											<div class="row">
												<label class="col-sm-3" for="exampleInputEmail1">Known
													Name <span class="required">&nbsp; *</span> </label>
												<div class="col-sm-7">
													<form:input class="form-control" placeholder=""
														path="knownname" id="knownname" maxlength="30"/>
													<form:errors path="knownname" cssClass="error" />
												</div>
											</div>
										</div>
										
										
										<div class="form-group">
											<div class="row">
												<label class="col-sm-3" for="exampleInputEmail1">User
													Name <span class="required">&nbsp; *</span> </label>
												<div class="col-sm-7">
													<form:input class="form-control" placeholder=""
														path="Username" id="username" maxlength="30"/>
													<form:errors path="Username" cssClass="error" />
												</div>
											</div>
										</div>
										
										
										<div class="form-group">
											<div class="row">
												<label class="col-sm-3" for="exampleInputEmail1">Password
													<span class="required">&nbsp; *</span></label>
												<div class="col-sm-7">
													<form:input class="form-control" placeholder=""
														path="Password" type="password" maxlength="8"/>
													<form:errors path="Password" cssClass="error" />
												</div>
											</div>
										</div>
										
										
										<div class="form-group">
											<div class="row">
												<label class="col-sm-3" for="exampleInputEmail1">Remarks
													</label>
												<div class="col-sm-7">
													<form:input class="form-control" placeholder=""
														path="remarks" maxlength="250"/>
													<form:errors path="remarks" cssClass="error" />
												</div>
											</div>
										</div>





									</div>



									<div class="clearfix"></div>
									<div class="space-25"></div>

									<div class="col-md-6">

										<div class="row">
											<div class="col-xs-3"></div>
											<div class="col-sm-2">
												<button type="submit" class="btn btn-sm btn-success">Submit</button>
											</div>
																																
											
											<div class="col-sm-2">
												<button type="button" id="clearbtn" class="btn btn-sm btn-warning">Clear</button>
											</div>
											
											<div class="col-sm-2">
												<button type="button"  id="returnbtn" class="btn btn-sm btn-info">Return</button>
											</div>
											
											
										</div>
									</div>


								</form:form>

								<!-- panel body end -->

							</div>
						</div>

					</div>
				</div>
				<!-- /.row -->

			</div>
			<!-- /.container-fluid -->

		</div>
		<!-- /#page-wrapper -->

	</div>
	<!-- /#wrapper -->

 	<div id="modal1" class="modal fade" role="dialog">
		<div class="modal-dialog modal-lg">

			
			<div class="modal-content">
				<div class="modal-header">
					<button type="button" class="close" data-dismiss="modal">&times;</button>
					<h4 class="modal-title">Reporting Officer</h4>
				</div>
				<div class="modal-body">

					<table class="table table-hover" id="tblref">
						
					</table>

				</div>
				<div class="modal-footer">
					<button type="button" class="btn btn-default" data-dismiss="modal">Close</button>
				</div>
			</div>

		</div>
	</div> 
	


	<div id="modal2" class="modal fade" role="dialog">
		<div class="modal-dialog modal-lg">

			<!-- Modal content-->
			<div class="modal-content">
				<div class="modal-header">
					<button type="button" class="close" data-dismiss="modal">&times;</button>
					<h4 class="modal-title">Department</h4>
				</div>
				<div class="modal-body">

					<table class="table table-hover" id="depttbl">

					</table>



				</div>
				<div class="modal-footer">
					<button type="button" class="btn btn-default" data-dismiss="modal">Close</button>
				</div>
			</div>

		</div>
	</div>

	<div id="modal3" class="modal fade" role="dialog">
		<div class="modal-dialog modal-lg">

			<!-- Modal content-->
			<div class="modal-content">
				<div class="modal-header">
					<button type="button" class="close" data-dismiss="modal">&times;</button>
					<h4 class="modal-title">Designation</h4>
				</div>
				<div class="modal-body">

					<table class="table table-hover" id="desigtbl">

					</table>



				</div>
				<div class="modal-footer">
					<button type="button" class="btn btn-default" data-dismiss="modal">Close</button>
				</div>
			</div>

		</div>
	</div>


	<div id="modal5" class="modal fade" role="dialog">
		<div class="modal-dialog modal-lg">

			<!-- Modal content-->
			<div class="modal-content">
				<div class="modal-header">
					<button type="button" class="close" data-dismiss="modal">&times;</button>
					<h4 class="modal-title">Shift Details</h4>
				</div>
				<div class="modal-body">

					<table class="table table-hover" id="shifttbl">

					</table> 



				</div>
				<div class="modal-footer">
					<button type="button" class="btn btn-default" data-dismiss="modal">Close</button>
				</div>
			</div>

		</div>
	</div>
	
	
	<div id="modal4" class="modal fade" role="dialog">
		<div class="modal-dialog modal-lg">

			
			<div class="modal-content">
				<div class="modal-header">
					<button type="button" class="close" data-dismiss="modal">&times;</button>
					<h4 class="modal-title">Alternate Reporting Officer</h4>
				</div>
				<div class="modal-body">

					<table class="table table-hover" id= "tblaltref">
					
					</table>



				</div>
				<div class="modal-footer">
					<button type="button" class="btn btn-default" data-dismiss="modal">Close</button>
				</div>
			</div>

		</div>
	</div> 




	<!-- jQuery -->
	<script src="<c:url value="/resources/js/jquery.js" />"></script>

	<!-- Bootstrap Core JavaScript -->
	<script src="<c:url value="/resources/js/bootstrap.min.js" />"></script>

	<script src="<c:url value="/resources/js/datatables.min.js" />"></script>
	
	<script src="<c:url value="/resources/js/navbar.js" />"></script>

	<script>
	
	
	   
	
		 $(document).ready(function() {
			 
			
			 
			 $("#empmobile").on("keypress input blur", function(event) {

           	  var value = $(this).val();
           	  value = value.replace(/\D+/, '');
           	  $(this).val(value);

             });
			 
			 
			 $("#emptp").on("keypress input blur", function(event) {

	           	  var value = $(this).val();
	           	  value = value.replace(/\D+/, '');
	           	  $(this).val(value);

	         });
			 
			 
			 $('#firstname').bind ("input propertychange", function () {
				 
				   var firstname = $('#firstname').val();
				   
				   $('#knownname').val(firstname);
				   				
				 				 			 
			 });
			 
			 
			 $('#employeetype').bind ("input propertychange", function () {
				 
				   var emptypeindex = $('#employeetype').val();
				   
				   var typeselect = document.getElementById("employeetype");
				   
				   var desc = typeselect.selectedOptions[0].label;

				   
				   if(desc==="Permanent"){
					   
					   var empno = $('#employeeNo').val();
					   var id = parseInt(empno, 10);
					   var fname = $('#firstname').val();
					   $('#username').val(fname+id);
					   
				   }
				   
				   else{
					   
					   var empno = $('#employeeNo').val();
					   var fname = $('#firstname').val();
					   
					   $('#username').val(fname+empno);
					   
				   }
				   				
				 				 			 
			 });
			 
			 			 
			 
			$("#tempdesig").keyup(function(){
	            	
				var desiginput = $('#tempdesig').val();
		   			 
		                if(desiginput == ""){
		    				 
		    				 $('#desigfield').val(null);
		    				 
		    				 
		    	        } 
		            	
		            	
		     }); 
			 
    
			 
			$("#tempdept").keyup(function(){
	            	
				  var deptinput = $('#tempdept').val();
	   			 
	                if(deptinput == ""){
	    				 
	    				 $('#deptfield').val(null);
	    				 
	    				 
	    	        } 
	            	
	            	
	         });
			 
			 
			 
            
            $("#tempshift").keyup(function(){
            	
            	var shiftinput =  $('#tempshift').val();
   			 
                if(shiftinput == ""){
    				 
    				 $('#shiftfield').val(null);
    				 
    				 
    			 } 
            	
            	
            });
            
            
             $("#temprptoff1").keyup(function(){
            	
            	var temprptoffinput =  $('#temprptoff1').val();
   			 
                if(temprptoffinput == ""){
    				 
    				 $('#rptoffid').val(null);
    				 
    				 
    			 } 
            	
            	
            });
            
            
            $("#temprptoff2").keyup(function(){
            	
            	var temprptoffinput2 =  $('#temprptoff2').val();
   			 
                if(temprptoffinput2 == ""){
    				 
    				 $('#altoffid').val(null);
    				 
    			 } 
                
            	
            }); 
            
			
			
			var officerTBL = $('#tblref').DataTable({
				"paging" : false,
				"ordering" : false,
				"info" : false,
				"search" : false,
				
				columns : [ 
				
				{
					title : ""
				},
				
				{
					title : "Officer ID"
				}, 
				
				{
					title : "Officer Name"
				}

				

				]
			});


			$('#tblref_filter').hide();
			
			
			$("#rptoffbtn1").click(function(){
			   
				 var rptoffname = $('#temprptoff1').val();
				 var rowcount = 0;
				 var obj;
				
				 officerTBL.clear().draw(); 
				 
				 $.ajax({
		                type: "GET",
		                url: "${pageContext.request.contextPath}/All/ReportingOfficers?rptname="+rptoffname+"",
		                success: function(response) {
		                   
		                	  obj = JSON.parse(response); 
		              
		                	  $.each(obj, function(key, value) {

			           	        	var strVar="";
			           	        	strVar += " <input type=\"radio\" name=\"test\" value=\"\">";


			    					 $('#tblref').DataTable().row.add(
			    								[strVar, value.userid , value.empfullname ])
			    								.draw(); 
			    					 
			    				});
		                	  
		                	  
		                	 rowcount = (officerTBL.page.info().recordsTotal);
		                	 
		                	 if(rowcount==1){
		 						
								 $('#rptoffid').val(obj[rowcount - 1].userid);
							     $('#temprptoff1').val(obj[rowcount - 1].empfullname);
								
							}
		                	
		                			                	
		                },
		                
		                async: false

		           });
				 
				
					if(rowcount != 1){
						
						 
						$('#modal1').modal({
							 
						    backdrop: 'static',
						    keyboard: false  
						    
					    });
						
					}
					
 				 				 				 
				 
				$('#tblref tbody').on( 'click', 'tr', function () {
					     var test = ( officerTBL.row( this ).data()[1] );
					     var temprpt1 = ( officerTBL.row( this ).data()[2] );
					     
					     $('#rptoffid').val(test);
					     $('#temprptoff1').val(temprpt1);
					     
					     $("#modal1 .close").click() 
				 
				});	
				
				
			}); 
			

			
		var altrefTBL = $('#tblaltref').DataTable({
			
				"paging" : false,
				"ordering" : false,
				"info" : false,
				"search" : false,
				
				columns : [ 
				
				{
					title : ""
				},
				
				{
					title : "Officer ID"
				}, 
				
				{
					title : "Officer Name"
				}
				

				]
		
			
			  });
 

			$('#tblaltref_filter').hide();
			

			
			$("#rptoffbtn2").click(function(){
			    
				 var rptoffname = $('#temprptoff2').val();
				 var rowcount = 0;
				 var obj;
				
				 altrefTBL.clear().draw(); 
				 
				 $.ajax({
					 
		                type: "GET",
		                url: "${pageContext.request.contextPath}/All/ReportingOfficers?rptname="+rptoffname+"",
		                		
		                success: function(response) {
		                   
		                	  obj = JSON.parse(response); 
		              
		                	  $.each(obj, function(key, value) {

			           	        	var strVar="";
			           	        	strVar += " <input type=\"radio\" name=\"test\" value=\"\">";


			    					 $('#tblaltref').DataTable().row.add(
			    								[strVar, value.userid , value.empfullname ])
			    								.draw(); 
			    					 
			    				});
		                	  
		                	  
			                	 rowcount = (altrefTBL.page.info().recordsTotal);
			                	 
			                	 if(rowcount==1){
			                		 
			 						
									 $('#altoffid').val(obj[rowcount - 1].userid);
								     $('#temprptoff2').val(obj[rowcount - 1].empfullname);
									
								}
		                	
		                			                	
		                },
		                
		                
		                async: false

		           });
				 
				 
				 if(rowcount != 1){
						
					 
						$('#modal4').modal({
							 
						    backdrop: 'static',
						    keyboard: false  
						    
					    });
						
				 }
				 
				 
				 $('#tblaltref tbody').on( 'click', 'tr', function () {
					 
				     var test = ( altrefTBL.row( this ).data()[1] );
				     var temprpt1 = ( altrefTBL.row( this ).data()[2] );
				    
				     $('#altoffid').val(test);
				     $('#temprptoff2').val(temprpt1);
				     
				     $("#modal4 .close").click() 
			 
			    });	
				 				
				
			}); 
			
			
	
		     var departmentTBL = $('#depttbl').DataTable({
					
					"paging" : false,
					"ordering" : false,
					"info" : false,
					"search" : false,
					
					columns : [ 
					
					{
						title : ""
					},
					
					{
						title : "Department ID"
					}, 
					
					{
						title : "Department Name"
					}
					
	
					]
				});
	
			$('#depttbl_filter').hide();
			
			
			$("#deptbtn").click(function() {
				
				
				var dept = $('#tempdept').val();
				departmentTBL.clear().draw(); 
				var rowcount = 0;
						
				
				$.ajax({
					type : "GET",
					url : "${pageContext.request.contextPath}/Dept/GetAll?deptname="+dept+" ",
				
					success : function(response) {
						
						var obj = JSON.parse(response);
						
					
	    				 $.each(obj, function(key, value) {

		           	        	  
	    					    var strVar="";
		           	        	strVar += " <input type=\"radio\" name=\"test\" value=\"\">";


		    					 $('#depttbl').DataTable().row.add(
		    								[strVar, value.deptid , value.deptname ])
		    								.draw();  
		           	        			           	       

	    			       });
	    				 
	    				    rowcount = (departmentTBL.page.info().recordsTotal);
	    				    
	    				    if(rowcount==1){
	    				    	
		 						
								 $('#deptfield').val(obj[rowcount - 1].deptid);
							     $('#tempdept').val(obj[rowcount - 1].deptname);
							     
								
							}
						
					     },
					     
					     async: false

				    });
				
				    
				    if(rowcount != 1){
				    	
				    	$('#modal2').modal({
							 
						    backdrop: 'static',
						    keyboard: false  
						    
					    });				    	
				    	
				    }
					 				 
				 
					$('#depttbl tbody').on( 'click', 'tr', function () {
						
					     var test = ( departmentTBL.row( this ).data()[1] );
					     var tempdeptname = ( departmentTBL.row( this ).data()[2] );
					    
					     $('#deptfield').val(test);
					     $('#tempdept').val(tempdeptname);
					     
					     $("#modal2 .close").click() 
				 
					});			
				 
				
				
			});
			
			
			
		    var desigTBL = $('#desigtbl').DataTable({
			  
					"paging" : false,
					"ordering" : false,
					"info" : false,
					"search" : false,
					
					columns : [ 
					
					{
						title : ""
					},
					
					{
						title : "Designation ID"
					}, 
					
					{
						title : "Designation Name"
					}

					
					]
		  
				});

				$('#desigtbl_filter').hide();
			
			
		
			   $("#desigbtn").click(function() {
				
                 
				var desig = $('#tempdesig').val();
				desigTBL.clear().draw(); 
				var rowcount = 0;
						
				
				$.ajax({
					type : "GET",
					url : "${pageContext.request.contextPath}/Desig/GetAll?designame="+desig+" ",
				
					success : function(response) {
						
						var obj = JSON.parse(response);
						
					
	    				 $.each(obj, function(key, value) {
	    					 

	    					 var strVar="";
		           	         strVar += " <input type=\"radio\" name=\"test\" value=\"\">";
	    				
	    					 
	    					 $('#desigtbl').DataTable().row.add(
	    								[strVar, value.desigid, value.designame ])
	    								.draw();
	    					 

	    			      });
	    				 
	    				 
	    				  rowcount = (desigTBL.page.info().recordsTotal);
	    				    
	    				    if(rowcount==1){
	    				    	
		 						
								 $('#desigfield').val(obj[rowcount - 1].desigid);
							     $('#tempdesig').val(obj[rowcount - 1].designame);
							     
								
						    }
	    				 
						
					 },
					 
					 async: false

				});
				
				 
				if(rowcount != 1){
					
					
					$('#modal3').modal({
						 
					    backdrop: 'static',
					    keyboard: false  
					    
				    });
					
				}
				
								
				$('#desigtbl tbody').on( 'click', 'tr', function () {
					
				     var test = ( desigTBL.row( this ).data()[1] );
				     var tempdesigname = ( desigTBL.row( this ).data()[2] );
				     
				     $('#desigfield').val(test);
				     $('#tempdesig').val(tempdesigname);
				     
				     $("#modal3 .close").click() 
			 
				});	
				
				
			});
			
			
			
		   var shiftTBL = $('#shifttbl').DataTable({
			
					"paging" : false,
					"ordering" : false,
					"info" : false,
					"search" : false,
					
					columns : [ 
					
					{
						title : ""
					},
					
					{
						title : "Shift ID"
					}, 
					
					{
						title : "Description"
					}
	
					]
	
		     });
	  

		     $('#shifttbl_filter').hide();
			
			
			
			$("#shiftbtn").click(function(){
				   
				
				var shiftn = $('#tempshift').val();
				var rowcount = 0;
				shiftTBL.clear().draw(); 
						
				
				$.ajax({
					
					type : "GET",
					url : "${pageContext.request.contextPath}/Shift/GetAll?shiftname="+shiftn+" ",
				
					success : function(response) {
						
						var obj = JSON.parse(response);
						
					
	    				 $.each(obj, function(key, value) {
		           	        	  
		           	        	  
		           	        	var strVar="";
		           	        	strVar += " <input type=\"radio\" name=\"test\" value=\"\">";
		           	        	  
			           	        
	    					 
		    				  $('#shifttbl').DataTable().row.add(
		    								[strVar, value.shiftid, value.description ])
		    								.draw();  
	    					 
	    			     });
	    				 
	    				 
	    				 rowcount = (shiftTBL.page.info().recordsTotal);
	                	 
	                	 if(rowcount==1){
	                		 
	 						
							 $('#shiftfield').val(obj[rowcount - 1].shiftid);
						     $('#tempshift').val(obj[rowcount - 1].description);
							
						}
	    				 
						
					},
					
					async: false

				}); 
				
				
				if(rowcount != 1){
					
					$('#modal5').modal({
						 
					    backdrop: 'static',
					    keyboard: false  
					    
				    });
										
				}
				
				
				$('#shifttbl tbody').on( 'click', 'tr', function () {
					
				     var test = ( shiftTBL.row( this ).data()[1] );
				     var tempshiftname = ( shiftTBL.row( this ).data()[2] );
				     
				      $('#shiftfield').val(test); 
				      $('#tempshift').val(tempshiftname); 
				      				       
				      $("#modal5 .close").click() 
			 
				});	
				
				
					
			}); 
			
			
			
			
			$( "#clearbtn" ).click(function() {
								
				 
				window.location.href = "${pageContext.request.contextPath}/Employee/Create";
				
				
			});
			
			
			
			$( "#returnbtn" ).click(function() {
				
				 
				window.location.href = "${pageContext.request.contextPath}/Employee/GetAll";
				
				
			});
			
			

		}); 
		 
		 
	</script>

</body>

</html>
