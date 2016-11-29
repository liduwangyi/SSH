package com.ssh.dao;

import org.hibernate.Query;
import org.hibernate.SessionFactory;

import com.ssh.entity.TUser;

public class UserDAOImpl implements UserDAO{

	private SessionFactory sessionFactory;
	
	public SessionFactory getSessionFactory() {
		return sessionFactory;
	}

	public void setSessionFactory(SessionFactory sessionFactory) {
		this.sessionFactory = sessionFactory;
	}

	@Override
	public TUser queryUserByName(String name) {
		// TODO Auto-generated method stub
		 Query query = sessionFactory.getCurrentSession().createQuery(
				 "from TUser as u where u.name = ?");        
		 query.setString(0, name);          
		 TUser u = (TUser) query.uniqueResult();        
		 return u;
	}

}
