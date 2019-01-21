package com.ONEzero.service;
import java.io.InputStream;
import java.sql.*;
import java.util.Properties;

import org.apache.log4j.Logger;

import com.microsoft.sqlserver.jdbc.SQLServerDriver;

public class DBUtil2 {
	
	private String connectionString;
    private static String resource = "DatabaseConfig.properties";
	
    private static DBUtil2 connectionFactory = null;
	
	
	private DBUtil2() {
		
		 ClassLoader loader = Thread.currentThread().getContextClassLoader();
	     Properties prop = new Properties();
		
		try {
			
			InputStream rs = loader.getResourceAsStream(resource);
			prop.load(rs);
			
			Class.forName(prop.getProperty("DB.classname"));
			
			connectionString = prop.getProperty("DB.connectionString");
		
		} catch (Exception e) {
			
			e.printStackTrace();
			
		}
		
	}
	
	public Connection getConnection(){
		
		Connection conn = null;
		
		try {
						
			conn = DriverManager.getConnection(connectionString);
			/*System.out.println("Database is Connected");*/
			
		} catch (Exception e) {
			
			e.printStackTrace();
			
		}
		
		
		return conn;
		
	}
	
	
	public static DBUtil2 getInstance() {
		
		if (connectionFactory == null) {
			
			connectionFactory = new DBUtil2();
			
		  }
		
		return connectionFactory;
		
     }
	

}
