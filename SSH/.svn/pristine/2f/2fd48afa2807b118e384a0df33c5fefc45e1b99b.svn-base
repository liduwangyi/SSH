package com.ssh.service;

import com.ssh.dao.UserDAO;
import com.ssh.entity.TUser;

public class UserServiceImpl implements UserService{

	private UserDAO userDAO; 
	
	public UserDAO getUserDAO() {
		return userDAO;
	}

	public void setUserDAO(UserDAO userDAO) {
		this.userDAO = userDAO;
	}

	@Override
	public boolean login(String name, String password) {
		// TODO Auto-generated method stub
		TUser u = userDAO.queryUserByName(name);         
		if (u == null) {             
			return false;        
		} else {              
			if (u.getPassword().equals(password)) 
			{                 
				return true;             
			} else 
			{                  
				return false;             
			}         
		}
	}

}
