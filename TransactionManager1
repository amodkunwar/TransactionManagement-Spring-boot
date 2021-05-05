package com.example.demo.exception;

import javax.persistence.EntityManagerFactory;
import javax.sql.DataSource;

import org.springframework.beans.factory.annotation.Qualifier;
import org.springframework.boot.autoconfigure.jdbc.DataSourceProperties;
import org.springframework.boot.context.properties.ConfigurationProperties;
import org.springframework.boot.jdbc.DataSourceBuilder;
import org.springframework.context.annotation.Bean;
import org.springframework.context.annotation.Configuration;
import org.springframework.data.jpa.repository.config.EnableJpaRepositories;
import org.springframework.orm.jpa.JpaTransactionManager;
import org.springframework.orm.jpa.LocalContainerEntityManagerFactoryBean;
import org.springframework.orm.jpa.vendor.HibernateJpaVendorAdapter;
import org.springframework.transaction.PlatformTransactionManager;
import org.springframework.transaction.annotation.EnableTransactionManagement;

@Configuration
@EnableTransactionManagement
@EnableJpaRepositories(basePackages = "", entityManagerFactoryRef = "transactionManagerFactory1", transactionManagerRef = "transactionManagerFactory1")
public class TransactionManager1 {

	/***
	 * @return specific data source properties for Schema1
	 */

	@Bean
	@ConfigurationProperties(value = "datasource.edge")
	public DataSourceProperties locdataSourceProperties() {
		return new DataSourceProperties();
	}

	/***
	 * Configuration for DataSource
	 * 
	 * @return dataSource initialized with the customizations defined on this
	 *         instance
	 */

	@Bean("dataSource")
	public DataSource dataSource() {
		DataSourceProperties dataSourceProperties = locdataSourceProperties();
		return DataSourceBuilder.create().driverClassName(dataSourceProperties.getDriverClassName())
				.url(dataSourceProperties.getUrl()).username(dataSourceProperties.getUsername())
				.password(dataSourceProperties.getPassword()).build();
	}

	/***
	 * 
	 * @param dataSource
	 * @param configServerRefresh
	 * @return
	 * 
	 *         Returning a currently active transaction or create a new one,
	 *         according to the specified propagation behaviour
	 * 
	 * @return transaction status object representing the new or current transaction
	 */

	@Bean
	public PlatformTransactionManager fxgLocEdgeTransactionManager(@Qualifier("dataSource") DataSource dataSource,
			ConnectionPoolingConfiguration configServerRefresh) {
		EntityManagerFactory entityManagerFactory = fxgLocEdgeEntityTransactionManager(dataSource, configServerRefresh)
				.getObject();
		return new JpaTransactionManager(entityManagerFactory);
	}

	/***
	 * 
	 * @param dataSource
	 * @param configServerRefresh
	 * @return
	 * 
	 *         Set the persistanceUnitManager to use for obtaining the JPA
	 *         persistence unit that this FactoryBean is supposed to build an
	 *         EntityManagerFactory for
	 * 
	 * @return object exposes additional metadata as assembled by this FactoryBean
	 */

	@Bean
	public LocalContainerEntityManagerFactoryBean fxgLocEdgeEntityTransactionManager(
			@Qualifier("dataSource") DataSource dataSource, ConnectionPoolingConfiguration configServerRefresh) {
		LocalContainerEntityManagerFactoryBean factory = new LocalContainerEntityManagerFactoryBean();
		factory.setDataSource(dataSource);
		factory.setPackagesToScan("edge.entity");
		factory.setJpaVendorAdapter(new HibernateJpaVendorAdapter());
		factory.setJpaProperties(configServerRefresh.getJpaProp1());
		return factory;
	}

}
