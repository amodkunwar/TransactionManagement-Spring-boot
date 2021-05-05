package com.example.demo.exception;

import java.util.Properties;

import org.springframework.beans.factory.annotation.Value;
import org.springframework.cloud.context.config.annotation.RefreshScope;
import org.springframework.context.annotation.Configuration;

@RefreshScope
@Configuration
public class ConnectionPoolingConfiguration {

	@Value("$(spring.jpa.show.sql)")
	private String jpaShowSql;

	@Value("$(spring.jpa.database.platform)")
	private String jpaDatabasePlatform;

	@Value("$(datasource.fxglocfoc.schema)")
	private String locFocSchema;

	@Value("$(spring.datasource.hikari.connectionTimeout)")
	private String hikariConnectionTimeout;

	@Value("$(spring.datasource.hikari.idleTimeout)")
	private String hikariIdleTimeout;

	@Value("$(spring.datasource.hikari.maxLifeTime)")
	private String hikariMaxLifeTime;

	@Value("$(spring.datasource.hikari.maximum-pool-size)")
	private String hikariMaximumPoolSize;

	@Value("$(spring.datasource.hikari.minimumIdle)")
	private String hikariMinimumIdle;

	@Value("$(spring.datasource.hikari.leakDetectionThreshold)")
	private String hikariLeakDetectionThreshold;

	@Value("$(datasource.edgeSchema)")
	private String edgeSchema;

	public String getJpaShowSql() {
		return jpaShowSql;
	}

	public void setJpaShowSql(String jpaShowSql) {
		this.jpaShowSql = jpaShowSql;
	}

	public String getJpaDatabasePlatform() {
		return jpaDatabasePlatform;
	}

	public void setJpaDatabasePlatform(String jpaDatabasePlatform) {
		this.jpaDatabasePlatform = jpaDatabasePlatform;
	}

	public String getLocFocSchema() {
		return locFocSchema;
	}

	public void setLocFocSchema(String locFocSchema) {
		this.locFocSchema = locFocSchema;
	}

	public String getHikariConnectionTimeout() {
		return hikariConnectionTimeout;
	}

	public void setHikariConnectionTimeout(String hikariConnectionTimeout) {
		this.hikariConnectionTimeout = hikariConnectionTimeout;
	}

	public String getHikariIdleTimeout() {
		return hikariIdleTimeout;
	}

	public void setHikariIdleTimeout(String hikariIdleTimeout) {
		this.hikariIdleTimeout = hikariIdleTimeout;
	}

	public String getHikariMaxLifeTime() {
		return hikariMaxLifeTime;
	}

	public void setHikariMaxLifeTime(String hikariMaxLifeTime) {
		this.hikariMaxLifeTime = hikariMaxLifeTime;
	}

	public String getHikariMaximumPoolSize() {
		return hikariMaximumPoolSize;
	}

	public void setHikariMaximumPoolSize(String hikariMaximumPoolSize) {
		this.hikariMaximumPoolSize = hikariMaximumPoolSize;
	}

	public String getHikariMinimumIdle() {
		return hikariMinimumIdle;
	}

	public void setHikariMinimumIdle(String hikariMinimumIdle) {
		this.hikariMinimumIdle = hikariMinimumIdle;
	}

	public String getHikariLeakDetectionThreshold() {
		return hikariLeakDetectionThreshold;
	}

	public void setHikariLeakDetectionThreshold(String hikariLeakDetectionThreshold) {
		this.hikariLeakDetectionThreshold = hikariLeakDetectionThreshold;
	}

	public String getEdgeSchema() {
		return edgeSchema;
	}

	public void setEdgeSchema(String edgeSchema) {
		this.edgeSchema = edgeSchema;
	}

	public Properties getJpaProp1() {
		Properties properties = new Properties();
		properties.put("spring.jpa.show.sql", jpaShowSql);
		properties.put("spring.jpa.database.platform", jpaDatabasePlatform);
		properties.put("hibernate.default_schema", edgeSchema);
		properties.put("hibernate.dialect", jpaDatabasePlatform);
		properties.put("spring.datasource.hikari.connectionTimeout", hikariConnectionTimeout);
		properties.put("spring.datasource.hikari.idleTimeout", hikariIdleTimeout);
		properties.put("spring.datasource.hikari.maxLifeTime", hikariMaxLifeTime);
		properties.put("spring.datasource.hikari.maximum-pool-size", hikariMaximumPoolSize);
		properties.put("spring.datasource.hikari.minimumIdle", hikariMinimumIdle);
		properties.put("spring.datasource.hikari.leakDetectionThreshold", hikariLeakDetectionThreshold);
		return properties;
	}

	public Properties getJpaProp2() {
		Properties properties = new Properties();
		properties.put("spring.jpa.show.sql", jpaShowSql);
		properties.put("spring.jpa.database.platform", jpaDatabasePlatform);
		properties.put("hibernate.default_schema", edgeSchema);
		properties.put("hibernate.dialect", jpaDatabasePlatform);
		properties.put("spring.datasource.hikari.connectionTimeout", hikariConnectionTimeout);
		properties.put("spring.datasource.hikari.idleTimeout", hikariIdleTimeout);
		properties.put("spring.datasource.hikari.maxLifeTime", hikariMaxLifeTime);
		properties.put("spring.datasource.hikari.maximum-pool-size", hikariMaximumPoolSize);
		properties.put("spring.datasource.hikari.minimumIdle", hikariMinimumIdle);
		properties.put("spring.datasource.hikari.leakDetectionThreshold", hikariLeakDetectionThreshold);
		return properties;
	}

}
