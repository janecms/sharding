[{
	"context": "application:8080",
	"parent": null,
	"beans": [{
		"bean": "providerUserApplication",
		"aliases": [],
		"scope": "singleton",
		"type": "com.hellojd.cloud.ProviderUserApplication$$EnhancerBySpringCGLIB$$b394e42f",
		"resource": "null",
		"dependencies": []
	},
	{
		"bean": "org.springframework.boot.autoconfigure.internalCachingMetadataReaderFactory",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.core.type.classreading.CachingMetadataReaderFactory",
		"resource": "null",
		"dependencies": []
	},
	{
		"bean": "userController",
		"aliases": [],
		"scope": "singleton",
		"type": "com.hellojd.cloud.controller.UserController",
		"resource": "file [G:/spring_cloud/microservice_simple_provider_user/target/classes/com/hellojd/cloud/controller/UserController.class]",
		"dependencies": ["userRepository"]
	},
	{
		"bean": "org.springframework.boot.autoconfigure.PropertyPlaceholderAutoConfiguration",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.autoconfigure.PropertyPlaceholderAutoConfiguration$$EnhancerBySpringCGLIB$$f80661d8",
		"resource": "null",
		"dependencies": []
	},
	{
		"bean": "org.springframework.boot.autoconfigure.condition.BeanTypeRegistry",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.autoconfigure.condition.BeanTypeRegistry$OptimizedBeanTypeRegistry",
		"resource": "null",
		"dependencies": []
	},
	{
		"bean": "propertySourcesPlaceholderConfigurer",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.context.support.PropertySourcesPlaceholderConfigurer",
		"resource": "class path resource [org/springframework/boot/autoconfigure/PropertyPlaceholderAutoConfiguration.class]",
		"dependencies": []
	},
	{
		"bean": "org.springframework.boot.autoconfigure.jackson.JacksonAutoConfiguration$Jackson2ObjectMapperBuilderCustomizerConfiguration",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.autoconfigure.jackson.JacksonAutoConfiguration$Jackson2ObjectMapperBuilderCustomizerConfiguration$$EnhancerBySpringCGLIB$$920e0f7",
		"resource": "null",
		"dependencies": []
	},
	{
		"bean": "standardJacksonObjectMapperBuilderCustomizer",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.autoconfigure.jackson.JacksonAutoConfiguration$Jackson2ObjectMapperBuilderCustomizerConfiguration$StandardJackson2ObjectMapperBuilderCustomizer",
		"resource": "class path resource [org/springframework/boot/autoconfigure/jackson/JacksonAutoConfiguration$Jackson2ObjectMapperBuilderCustomizerConfiguration.class]",
		"dependencies": ["org.springframework.boot.context.embedded.AnnotationConfigEmbeddedWebApplicationContext@27d14185",
		"spring.jackson-org.springframework.boot.autoconfigure.jackson.JacksonProperties"]
	},
	{
		"bean": "spring.jackson-org.springframework.boot.autoconfigure.jackson.JacksonProperties",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.autoconfigure.jackson.JacksonProperties",
		"resource": "null",
		"dependencies": []
	},
	{
		"bean": "org.springframework.boot.context.properties.ConfigurationPropertiesBindingPostProcessor",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.context.properties.ConfigurationPropertiesBindingPostProcessor",
		"resource": "null",
		"dependencies": ["org.springframework.boot.context.properties.ConfigurationPropertiesBindingPostProcessor.store"]
	},
	{
		"bean": "org.springframework.boot.context.properties.ConfigurationPropertiesBindingPostProcessor.store",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.context.properties.ConfigurationBeanFactoryMetaData",
		"resource": "null",
		"dependencies": []
	},
	{
		"bean": "org.springframework.boot.autoconfigure.jackson.JacksonAutoConfiguration$JacksonObjectMapperBuilderConfiguration",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.autoconfigure.jackson.JacksonAutoConfiguration$JacksonObjectMapperBuilderConfiguration$$EnhancerBySpringCGLIB$$4e09fb08",
		"resource": "null",
		"dependencies": ["org.springframework.boot.context.embedded.AnnotationConfigEmbeddedWebApplicationContext@27d14185",
		"spring.jackson-org.springframework.boot.autoconfigure.jackson.JacksonProperties",
		"standardJacksonObjectMapperBuilderCustomizer"]
	},
	{
		"bean": "jacksonObjectMapperBuilder",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.http.converter.json.Jackson2ObjectMapperBuilder",
		"resource": "class path resource [org/springframework/boot/autoconfigure/jackson/JacksonAutoConfiguration$JacksonObjectMapperBuilderConfiguration.class]",
		"dependencies": ["standardJacksonObjectMapperBuilderCustomizer"]
	},
	{
		"bean": "org.springframework.boot.autoconfigure.jackson.JacksonAutoConfiguration$JacksonObjectMapperConfiguration",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.autoconfigure.jackson.JacksonAutoConfiguration$JacksonObjectMapperConfiguration$$EnhancerBySpringCGLIB$$9bbd38ef",
		"resource": "null",
		"dependencies": []
	},
	{
		"bean": "jacksonObjectMapper",
		"aliases": [],
		"scope": "singleton",
		"type": "com.fasterxml.jackson.databind.ObjectMapper",
		"resource": "class path resource [org/springframework/boot/autoconfigure/jackson/JacksonAutoConfiguration$JacksonObjectMapperConfiguration.class]",
		"dependencies": ["jacksonObjectMapperBuilder"]
	},
	{
		"bean": "org.springframework.boot.autoconfigure.jackson.JacksonAutoConfiguration",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.autoconfigure.jackson.JacksonAutoConfiguration$$EnhancerBySpringCGLIB$$7dc8d67e",
		"resource": "null",
		"dependencies": []
	},
	{
		"bean": "jsonComponentModule",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.jackson.JsonComponentModule",
		"resource": "class path resource [org/springframework/boot/autoconfigure/jackson/JacksonAutoConfiguration.class]",
		"dependencies": []
	},
	{
		"bean": "org.springframework.boot.autoconfigure.websocket.WebSocketAutoConfiguration$TomcatWebSocketConfiguration",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.autoconfigure.websocket.WebSocketAutoConfiguration$TomcatWebSocketConfiguration$$EnhancerBySpringCGLIB$$6efc3987",
		"resource": "null",
		"dependencies": []
	},
	{
		"bean": "websocketContainerCustomizer",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.autoconfigure.websocket.TomcatWebSocketContainerCustomizer",
		"resource": "class path resource [org/springframework/boot/autoconfigure/websocket/WebSocketAutoConfiguration$TomcatWebSocketConfiguration.class]",
		"dependencies": []
	},
	{
		"bean": "org.springframework.boot.autoconfigure.websocket.WebSocketAutoConfiguration",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.autoconfigure.websocket.WebSocketAutoConfiguration$$EnhancerBySpringCGLIB$$52da4db6",
		"resource": "null",
		"dependencies": []
	},
	{
		"bean": "org.springframework.boot.autoconfigure.web.EmbeddedServletContainerAutoConfiguration$EmbeddedTomcat",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.autoconfigure.web.EmbeddedServletContainerAutoConfiguration$EmbeddedTomcat$$EnhancerBySpringCGLIB$$f3acfc7a",
		"resource": "null",
		"dependencies": []
	},
	{
		"bean": "tomcatEmbeddedServletContainerFactory",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.context.embedded.tomcat.TomcatEmbeddedServletContainerFactory",
		"resource": "class path resource [org/springframework/boot/autoconfigure/web/EmbeddedServletContainerAutoConfiguration$EmbeddedTomcat.class]",
		"dependencies": []
	},
	{
		"bean": "org.springframework.boot.autoconfigure.web.EmbeddedServletContainerAutoConfiguration",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.autoconfigure.web.EmbeddedServletContainerAutoConfiguration$$EnhancerBySpringCGLIB$$ac96899e",
		"resource": "null",
		"dependencies": []
	},
	{
		"bean": "embeddedServletContainerCustomizerBeanPostProcessor",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.context.embedded.EmbeddedServletContainerCustomizerBeanPostProcessor",
		"resource": "null",
		"dependencies": []
	},
	{
		"bean": "errorPageRegistrarBeanPostProcessor",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.web.servlet.ErrorPageRegistrarBeanPostProcessor",
		"resource": "null",
		"dependencies": []
	},
	{
		"bean": "org.springframework.boot.autoconfigure.web.DispatcherServletAutoConfiguration$DispatcherServletConfiguration",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.autoconfigure.web.DispatcherServletAutoConfiguration$DispatcherServletConfiguration$$EnhancerBySpringCGLIB$$e68f68b0",
		"resource": "null",
		"dependencies": ["spring.mvc-org.springframework.boot.autoconfigure.web.WebMvcProperties"]
	},
	{
		"bean": "dispatcherServlet",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.web.servlet.DispatcherServlet",
		"resource": "class path resource [org/springframework/boot/autoconfigure/web/DispatcherServletAutoConfiguration$DispatcherServletConfiguration.class]",
		"dependencies": []
	},
	{
		"bean": "spring.mvc-org.springframework.boot.autoconfigure.web.WebMvcProperties",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.autoconfigure.web.WebMvcProperties",
		"resource": "null",
		"dependencies": []
	},
	{
		"bean": "org.springframework.boot.autoconfigure.web.DispatcherServletAutoConfiguration$DispatcherServletRegistrationConfiguration",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.autoconfigure.web.DispatcherServletAutoConfiguration$DispatcherServletRegistrationConfiguration$$EnhancerBySpringCGLIB$$617ef7d7",
		"resource": "null",
		"dependencies": ["serverProperties",
		"spring.mvc-org.springframework.boot.autoconfigure.web.WebMvcProperties"]
	},
	{
		"bean": "dispatcherServletRegistration",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.web.servlet.ServletRegistrationBean",
		"resource": "class path resource [org/springframework/boot/autoconfigure/web/DispatcherServletAutoConfiguration$DispatcherServletRegistrationConfiguration.class]",
		"dependencies": ["dispatcherServlet"]
	},
	{
		"bean": "org.springframework.boot.autoconfigure.web.DispatcherServletAutoConfiguration",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.autoconfigure.web.DispatcherServletAutoConfiguration$$EnhancerBySpringCGLIB$$359dfbb2",
		"resource": "null",
		"dependencies": []
	},
	{
		"bean": "org.springframework.boot.autoconfigure.web.ErrorMvcAutoConfiguration$WhitelabelErrorViewConfiguration",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.autoconfigure.web.ErrorMvcAutoConfiguration$WhitelabelErrorViewConfiguration$$EnhancerBySpringCGLIB$$86712acc",
		"resource": "null",
		"dependencies": []
	},
	{
		"bean": "error",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.autoconfigure.web.ErrorMvcAutoConfiguration$SpelView",
		"resource": "class path resource [org/springframework/boot/autoconfigure/web/ErrorMvcAutoConfiguration$WhitelabelErrorViewConfiguration.class]",
		"dependencies": []
	},
	{
		"bean": "beanNameViewResolver",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.web.servlet.view.BeanNameViewResolver",
		"resource": "class path resource [org/springframework/boot/autoconfigure/web/ErrorMvcAutoConfiguration$WhitelabelErrorViewConfiguration.class]",
		"dependencies": []
	},
	{
		"bean": "org.springframework.boot.autoconfigure.web.ErrorMvcAutoConfiguration",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.autoconfigure.web.ErrorMvcAutoConfiguration$$EnhancerBySpringCGLIB$$f624c352",
		"resource": "null",
		"dependencies": ["org.springframework.boot.context.embedded.AnnotationConfigEmbeddedWebApplicationContext@27d14185",
		"serverProperties",
		"spring.resources-org.springframework.boot.autoconfigure.web.ResourceProperties",
		"conventionErrorViewResolver"]
	},
	{
		"bean": "errorAttributes",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.autoconfigure.web.DefaultErrorAttributes",
		"resource": "class path resource [org/springframework/boot/autoconfigure/web/ErrorMvcAutoConfiguration.class]",
		"dependencies": []
	},
	{
		"bean": "basicErrorController",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.autoconfigure.web.BasicErrorController",
		"resource": "class path resource [org/springframework/boot/autoconfigure/web/ErrorMvcAutoConfiguration.class]",
		"dependencies": ["errorAttributes"]
	},
	{
		"bean": "errorPageCustomizer",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.autoconfigure.web.ErrorMvcAutoConfiguration$ErrorPageCustomizer",
		"resource": "class path resource [org/springframework/boot/autoconfigure/web/ErrorMvcAutoConfiguration.class]",
		"dependencies": []
	},
	{
		"bean": "conventionErrorViewResolver",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.autoconfigure.web.DefaultErrorViewResolver",
		"resource": "class path resource [org/springframework/boot/autoconfigure/web/ErrorMvcAutoConfiguration.class]",
		"dependencies": []
	},
	{
		"bean": "preserveErrorControllerTargetClassPostProcessor",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.autoconfigure.web.ErrorMvcAutoConfiguration$PreserveErrorControllerTargetClassPostProcessor",
		"resource": "class path resource [org/springframework/boot/autoconfigure/web/ErrorMvcAutoConfiguration.class]",
		"dependencies": []
	},
	{
		"bean": "spring.resources-org.springframework.boot.autoconfigure.web.ResourceProperties",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.autoconfigure.web.ResourceProperties",
		"resource": "null",
		"dependencies": []
	},
	{
		"bean": "org.springframework.boot.autoconfigure.web.WebMvcAutoConfiguration$EnableWebMvcConfiguration",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.autoconfigure.web.WebMvcAutoConfiguration$EnableWebMvcConfiguration$$EnhancerBySpringCGLIB$$97575b67",
		"resource": "null",
		"dependencies": ["org.springframework.beans.factory.support.DefaultListableBeanFactory@21f58f66",
		"org.springframework.boot.autoconfigure.web.WebMvcAutoConfiguration$WebMvcAutoConfigurationAdapter",
		"org.springframework.boot.autoconfigure.orm.jpa.JpaBaseConfiguration$JpaWebConfiguration$JpaWebMvcConfiguration",
		"heapdumpMvcEndpoint",
		"org.springframework.data.web.config.SpringDataWebConfiguration"]
	},
	{
		"bean": "requestMappingHandlerAdapter",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.web.servlet.mvc.method.annotation.RequestMappingHandlerAdapter",
		"resource": "class path resource [org/springframework/boot/autoconfigure/web/WebMvcAutoConfiguration$EnableWebMvcConfiguration.class]",
		"dependencies": []
	},
	{
		"bean": "requestMappingHandlerMapping",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.web.servlet.mvc.method.annotation.RequestMappingHandlerMapping",
		"resource": "class path resource [org/springframework/boot/autoconfigure/web/WebMvcAutoConfiguration$EnableWebMvcConfiguration.class]",
		"dependencies": []
	},
	{
		"bean": "mvcPathMatcher",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.util.AntPathMatcher",
		"resource": "class path resource [org/springframework/boot/autoconfigure/web/WebMvcAutoConfiguration$EnableWebMvcConfiguration.class]",
		"dependencies": []
	},
	{
		"bean": "mvcUrlPathHelper",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.web.util.UrlPathHelper",
		"resource": "class path resource [org/springframework/boot/autoconfigure/web/WebMvcAutoConfiguration$EnableWebMvcConfiguration.class]",
		"dependencies": []
	},
	{
		"bean": "mvcContentNegotiationManager",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.web.accept.ContentNegotiationManager",
		"resource": "class path resource [org/springframework/boot/autoconfigure/web/WebMvcAutoConfiguration$EnableWebMvcConfiguration.class]",
		"dependencies": []
	},
	{
		"bean": "viewControllerHandlerMapping",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.web.servlet.config.annotation.WebMvcConfigurationSupport$EmptyHandlerMapping",
		"resource": "class path resource [org/springframework/boot/autoconfigure/web/WebMvcAutoConfiguration$EnableWebMvcConfiguration.class]",
		"dependencies": []
	},
	{
		"bean": "beanNameHandlerMapping",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.web.servlet.handler.BeanNameUrlHandlerMapping",
		"resource": "class path resource [org/springframework/boot/autoconfigure/web/WebMvcAutoConfiguration$EnableWebMvcConfiguration.class]",
		"dependencies": []
	},
	{
		"bean": "resourceHandlerMapping",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.web.servlet.handler.SimpleUrlHandlerMapping",
		"resource": "class path resource [org/springframework/boot/autoconfigure/web/WebMvcAutoConfiguration$EnableWebMvcConfiguration.class]",
		"dependencies": []
	},
	{
		"bean": "mvcResourceUrlProvider",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.web.servlet.resource.ResourceUrlProvider",
		"resource": "class path resource [org/springframework/boot/autoconfigure/web/WebMvcAutoConfiguration$EnableWebMvcConfiguration.class]",
		"dependencies": []
	},
	{
		"bean": "defaultServletHandlerMapping",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.web.servlet.config.annotation.WebMvcConfigurationSupport$EmptyHandlerMapping",
		"resource": "class path resource [org/springframework/boot/autoconfigure/web/WebMvcAutoConfiguration$EnableWebMvcConfiguration.class]",
		"dependencies": []
	},
	{
		"bean": "mvcConversionService",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.format.support.DefaultFormattingConversionService",
		"resource": "class path resource [org/springframework/boot/autoconfigure/web/WebMvcAutoConfiguration$EnableWebMvcConfiguration.class]",
		"dependencies": []
	},
	{
		"bean": "mvcValidator",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.validation.beanvalidation.OptionalValidatorFactoryBean",
		"resource": "class path resource [org/springframework/boot/autoconfigure/web/WebMvcAutoConfiguration$EnableWebMvcConfiguration.class]",
		"dependencies": []
	},
	{
		"bean": "mvcUriComponentsContributor",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.web.method.support.CompositeUriComponentsContributor",
		"resource": "class path resource [org/springframework/boot/autoconfigure/web/WebMvcAutoConfiguration$EnableWebMvcConfiguration.class]",
		"dependencies": []
	},
	{
		"bean": "httpRequestHandlerAdapter",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.web.servlet.mvc.HttpRequestHandlerAdapter",
		"resource": "class path resource [org/springframework/boot/autoconfigure/web/WebMvcAutoConfiguration$EnableWebMvcConfiguration.class]",
		"dependencies": []
	},
	{
		"bean": "simpleControllerHandlerAdapter",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.web.servlet.mvc.SimpleControllerHandlerAdapter",
		"resource": "class path resource [org/springframework/boot/autoconfigure/web/WebMvcAutoConfiguration$EnableWebMvcConfiguration.class]",
		"dependencies": []
	},
	{
		"bean": "handlerExceptionResolver",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.web.servlet.handler.HandlerExceptionResolverComposite",
		"resource": "class path resource [org/springframework/boot/autoconfigure/web/WebMvcAutoConfiguration$EnableWebMvcConfiguration.class]",
		"dependencies": []
	},
	{
		"bean": "mvcViewResolver",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.web.servlet.view.ViewResolverComposite",
		"resource": "class path resource [org/springframework/boot/autoconfigure/web/WebMvcAutoConfiguration$EnableWebMvcConfiguration.class]",
		"dependencies": []
	},
	{
		"bean": "org.springframework.boot.autoconfigure.web.WebMvcAutoConfiguration$WebMvcAutoConfigurationAdapter$FaviconConfiguration",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.autoconfigure.web.WebMvcAutoConfiguration$WebMvcAutoConfigurationAdapter$FaviconConfiguration$$EnhancerBySpringCGLIB$$7846e552",
		"resource": "null",
		"dependencies": ["spring.resources-org.springframework.boot.autoconfigure.web.ResourceProperties"]
	},
	{
		"bean": "faviconHandlerMapping",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.web.servlet.handler.SimpleUrlHandlerMapping",
		"resource": "class path resource [org/springframework/boot/autoconfigure/web/WebMvcAutoConfiguration$WebMvcAutoConfigurationAdapter$FaviconConfiguration.class]",
		"dependencies": []
	},
	{
		"bean": "faviconRequestHandler",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.web.servlet.resource.ResourceHttpRequestHandler",
		"resource": "class path resource [org/springframework/boot/autoconfigure/web/WebMvcAutoConfiguration$WebMvcAutoConfigurationAdapter$FaviconConfiguration.class]",
		"dependencies": []
	},
	{
		"bean": "org.springframework.boot.autoconfigure.web.WebMvcAutoConfiguration$WebMvcAutoConfigurationAdapter",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.autoconfigure.web.WebMvcAutoConfiguration$WebMvcAutoConfigurationAdapter$$EnhancerBySpringCGLIB$$2b2d10da",
		"resource": "null",
		"dependencies": ["spring.resources-org.springframework.boot.autoconfigure.web.ResourceProperties",
		"spring.mvc-org.springframework.boot.autoconfigure.web.WebMvcProperties",
		"org.springframework.beans.factory.support.DefaultListableBeanFactory@21f58f66",
		"messageConverters"]
	},
	{
		"bean": "defaultViewResolver",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.web.servlet.view.InternalResourceViewResolver",
		"resource": "class path resource [org/springframework/boot/autoconfigure/web/WebMvcAutoConfiguration$WebMvcAutoConfigurationAdapter.class]",
		"dependencies": []
	},
	{
		"bean": "viewResolver",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.web.servlet.view.ContentNegotiatingViewResolver",
		"resource": "class path resource [org/springframework/boot/autoconfigure/web/WebMvcAutoConfiguration$WebMvcAutoConfigurationAdapter.class]",
		"dependencies": ["org.springframework.beans.factory.support.DefaultListableBeanFactory@21f58f66"]
	},
	{
		"bean": "welcomePageHandlerMapping",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.autoconfigure.web.WebMvcAutoConfiguration$WelcomePageHandlerMapping",
		"resource": "class path resource [org/springframework/boot/autoconfigure/web/WebMvcAutoConfiguration$WebMvcAutoConfigurationAdapter.class]",
		"dependencies": ["spring.resources-org.springframework.boot.autoconfigure.web.ResourceProperties"]
	},
	{
		"bean": "requestContextFilter",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.web.filter.OrderedRequestContextFilter",
		"resource": "class path resource [org/springframework/boot/autoconfigure/web/WebMvcAutoConfiguration$WebMvcAutoConfigurationAdapter.class]",
		"dependencies": []
	},
	{
		"bean": "org.springframework.boot.autoconfigure.web.WebMvcAutoConfiguration",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.autoconfigure.web.WebMvcAutoConfiguration$$EnhancerBySpringCGLIB$$af66a29e",
		"resource": "null",
		"dependencies": []
	},
	{
		"bean": "hiddenHttpMethodFilter",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.web.filter.OrderedHiddenHttpMethodFilter",
		"resource": "class path resource [org/springframework/boot/autoconfigure/web/WebMvcAutoConfiguration.class]",
		"dependencies": []
	},
	{
		"bean": "httpPutFormContentFilter",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.web.filter.OrderedHttpPutFormContentFilter",
		"resource": "class path resource [org/springframework/boot/autoconfigure/web/WebMvcAutoConfiguration.class]",
		"dependencies": []
	},
	{
		"bean": "org.springframework.boot.actuate.autoconfigure.AuditAutoConfiguration$AuditEventRepositoryConfiguration",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.actuate.autoconfigure.AuditAutoConfiguration$AuditEventRepositoryConfiguration",
		"resource": "null",
		"dependencies": []
	},
	{
		"bean": "auditEventRepository",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.actuate.audit.InMemoryAuditEventRepository",
		"resource": "class path resource [org/springframework/boot/actuate/autoconfigure/AuditAutoConfiguration$AuditEventRepositoryConfiguration.class]",
		"dependencies": []
	},
	{
		"bean": "org.springframework.boot.actuate.autoconfigure.AuditAutoConfiguration",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.actuate.autoconfigure.AuditAutoConfiguration$$EnhancerBySpringCGLIB$$e374af3a",
		"resource": "null",
		"dependencies": []
	},
	{
		"bean": "auditListener",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.actuate.audit.listener.AuditListener",
		"resource": "class path resource [org/springframework/boot/actuate/autoconfigure/AuditAutoConfiguration.class]",
		"dependencies": []
	},
	{
		"bean": "org.springframework.boot.autoconfigure.transaction.jta.JtaAutoConfiguration",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.autoconfigure.transaction.jta.JtaAutoConfiguration",
		"resource": "null",
		"dependencies": []
	},
	{
		"bean": "spring.jta-org.springframework.boot.autoconfigure.transaction.jta.JtaProperties",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.autoconfigure.transaction.jta.JtaProperties",
		"resource": "null",
		"dependencies": []
	},
	{
		"bean": "org.springframework.boot.autoconfigure.jdbc.DataSourceConfiguration$Tomcat",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.autoconfigure.jdbc.DataSourceConfiguration$Tomcat",
		"resource": "null",
		"dependencies": []
	},
	{
		"bean": "dataSource",
		"aliases": [],
		"scope": "singleton",
		"type": "org.apache.tomcat.jdbc.pool.DataSource",
		"resource": "class path resource [org/springframework/boot/autoconfigure/jdbc/DataSourceConfiguration$Tomcat.class]",
		"dependencies": ["spring.datasource-org.springframework.boot.autoconfigure.jdbc.DataSourceProperties"]
	},
	{
		"bean": "org.springframework.boot.autoconfigure.jdbc.DataSourceAutoConfiguration$PooledDataSourceConfiguration",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.autoconfigure.jdbc.DataSourceAutoConfiguration$PooledDataSourceConfiguration$$EnhancerBySpringCGLIB$$becdaa50",
		"resource": "null",
		"dependencies": []
	},
	{
		"bean": "org.springframework.boot.autoconfigure.jdbc.metadata.DataSourcePoolMetadataProvidersConfiguration$TomcatDataSourcePoolMetadataProviderConfiguration",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.autoconfigure.jdbc.metadata.DataSourcePoolMetadataProvidersConfiguration$TomcatDataSourcePoolMetadataProviderConfiguration$$EnhancerBySpringCGLIB$$9f8fa78c",
		"resource": "null",
		"dependencies": []
	},
	{
		"bean": "tomcatPoolDataSourceMetadataProvider",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.autoconfigure.jdbc.metadata.DataSourcePoolMetadataProvidersConfiguration$TomcatDataSourcePoolMetadataProviderConfiguration$1",
		"resource": "class path resource [org/springframework/boot/autoconfigure/jdbc/metadata/DataSourcePoolMetadataProvidersConfiguration$TomcatDataSourcePoolMetadataProviderConfiguration.class]",
		"dependencies": []
	},
	{
		"bean": "org.springframework.boot.autoconfigure.jdbc.metadata.DataSourcePoolMetadataProvidersConfiguration",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.autoconfigure.jdbc.metadata.DataSourcePoolMetadataProvidersConfiguration$$EnhancerBySpringCGLIB$$1d1aa19f",
		"resource": "null",
		"dependencies": []
	},
	{
		"bean": "org.springframework.boot.autoconfigure.jdbc.DataSourceAutoConfiguration",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.autoconfigure.jdbc.DataSourceAutoConfiguration$$EnhancerBySpringCGLIB$$221d5cbe",
		"resource": "null",
		"dependencies": []
	},
	{
		"bean": "dataSourceInitializer",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.autoconfigure.jdbc.DataSourceInitializer",
		"resource": "class path resource [org/springframework/boot/autoconfigure/jdbc/DataSourceAutoConfiguration.class]",
		"dependencies": ["spring.datasource-org.springframework.boot.autoconfigure.jdbc.DataSourceProperties"]
	},
	{
		"bean": "spring.datasource-org.springframework.boot.autoconfigure.jdbc.DataSourceProperties",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.autoconfigure.jdbc.DataSourceProperties",
		"resource": "null",
		"dependencies": []
	},
	{
		"bean": "org.springframework.boot.autoconfigure.orm.jpa.JpaBaseConfiguration$JpaWebConfiguration$JpaWebMvcConfiguration",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.autoconfigure.orm.jpa.JpaBaseConfiguration$JpaWebConfiguration$JpaWebMvcConfiguration$$EnhancerBySpringCGLIB$$8964c656",
		"resource": "null",
		"dependencies": []
	},
	{
		"bean": "openEntityManagerInViewInterceptor",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.orm.jpa.support.OpenEntityManagerInViewInterceptor",
		"resource": "class path resource [org/springframework/boot/autoconfigure/orm/jpa/JpaBaseConfiguration$JpaWebConfiguration$JpaWebMvcConfiguration.class]",
		"dependencies": []
	},
	{
		"bean": "org.springframework.boot.autoconfigure.orm.jpa.JpaBaseConfiguration$JpaWebConfiguration",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.autoconfigure.orm.jpa.JpaBaseConfiguration$JpaWebConfiguration$$EnhancerBySpringCGLIB$$ae4656a9",
		"resource": "null",
		"dependencies": []
	},
	{
		"bean": "org.springframework.boot.autoconfigure.orm.jpa.HibernateJpaAutoConfiguration",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.autoconfigure.orm.jpa.HibernateJpaAutoConfiguration$$EnhancerBySpringCGLIB$$a9b01d7e",
		"resource": "null",
		"dependencies": ["dataSource",
		"spring.jpa-org.springframework.boot.autoconfigure.orm.jpa.JpaProperties"]
	},
	{
		"bean": "transactionManager",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.orm.jpa.JpaTransactionManager",
		"resource": "class path resource [org/springframework/boot/autoconfigure/orm/jpa/HibernateJpaAutoConfiguration.class]",
		"dependencies": []
	},
	{
		"bean": "jpaVendorAdapter",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.orm.jpa.vendor.HibernateJpaVendorAdapter",
		"resource": "class path resource [org/springframework/boot/autoconfigure/orm/jpa/HibernateJpaAutoConfiguration.class]",
		"dependencies": []
	},
	{
		"bean": "entityManagerFactoryBuilder",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.orm.jpa.EntityManagerFactoryBuilder",
		"resource": "class path resource [org/springframework/boot/autoconfigure/orm/jpa/HibernateJpaAutoConfiguration.class]",
		"dependencies": ["jpaVendorAdapter"]
	},
	{
		"bean": "entityManagerFactory",
		"aliases": [],
		"scope": "singleton",
		"type": "com.sun.proxy.$Proxy100",
		"resource": "class path resource [org/springframework/boot/autoconfigure/orm/jpa/HibernateJpaAutoConfiguration.class]",
		"dependencies": ["entityManagerFactoryBuilder"]
	},
	{
		"bean": "spring.jpa-org.springframework.boot.autoconfigure.orm.jpa.JpaProperties",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.autoconfigure.orm.jpa.JpaProperties",
		"resource": "null",
		"dependencies": []
	},
	{
		"bean": "org.springframework.boot.autoconfigure.info.ProjectInfoAutoConfiguration",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.autoconfigure.info.ProjectInfoAutoConfiguration$$EnhancerBySpringCGLIB$$7c23c677",
		"resource": "null",
		"dependencies": ["spring.info-org.springframework.boot.autoconfigure.info.ProjectInfoProperties"]
	},
	{
		"bean": "spring.info-org.springframework.boot.autoconfigure.info.ProjectInfoProperties",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.autoconfigure.info.ProjectInfoProperties",
		"resource": "null",
		"dependencies": []
	},
	{
		"bean": "org.springframework.boot.actuate.autoconfigure.InfoContributorAutoConfiguration",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.actuate.autoconfigure.InfoContributorAutoConfiguration$$EnhancerBySpringCGLIB$$e9908408",
		"resource": "null",
		"dependencies": ["management.info-org.springframework.boot.actuate.autoconfigure.InfoContributorProperties"]
	},
	{
		"bean": "envInfoContributor",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.actuate.info.EnvironmentInfoContributor",
		"resource": "class path resource [org/springframework/boot/actuate/autoconfigure/InfoContributorAutoConfiguration.class]",
		"dependencies": ["environment"]
	},
	{
		"bean": "management.info-org.springframework.boot.actuate.autoconfigure.InfoContributorProperties",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.actuate.autoconfigure.InfoContributorProperties",
		"resource": "null",
		"dependencies": []
	},
	{
		"bean": "org.springframework.boot.actuate.autoconfigure.HealthIndicatorAutoConfiguration$DiskSpaceHealthIndicatorConfiguration",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.actuate.autoconfigure.HealthIndicatorAutoConfiguration$DiskSpaceHealthIndicatorConfiguration$$EnhancerBySpringCGLIB$$e55324ea",
		"resource": "null",
		"dependencies": []
	},
	{
		"bean": "diskSpaceHealthIndicator",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.actuate.health.DiskSpaceHealthIndicator",
		"resource": "class path resource [org/springframework/boot/actuate/autoconfigure/HealthIndicatorAutoConfiguration$DiskSpaceHealthIndicatorConfiguration.class]",
		"dependencies": ["diskSpaceHealthIndicatorProperties"]
	},
	{
		"bean": "diskSpaceHealthIndicatorProperties",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.actuate.health.DiskSpaceHealthIndicatorProperties",
		"resource": "class path resource [org/springframework/boot/actuate/autoconfigure/HealthIndicatorAutoConfiguration$DiskSpaceHealthIndicatorConfiguration.class]",
		"dependencies": []
	},
	{
		"bean": "org.springframework.boot.actuate.autoconfigure.HealthIndicatorAutoConfiguration$DataSourcesHealthIndicatorConfiguration",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.actuate.autoconfigure.HealthIndicatorAutoConfiguration$DataSourcesHealthIndicatorConfiguration$$EnhancerBySpringCGLIB$$7916138f",
		"resource": "null",
		"dependencies": ["healthAggregator"]
	},
	{
		"bean": "dbHealthIndicator",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.actuate.health.DataSourceHealthIndicator",
		"resource": "class path resource [org/springframework/boot/actuate/autoconfigure/HealthIndicatorAutoConfiguration$DataSourcesHealthIndicatorConfiguration.class]",
		"dependencies": []
	},
	{
		"bean": "org.springframework.boot.actuate.autoconfigure.HealthIndicatorAutoConfiguration",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.actuate.autoconfigure.HealthIndicatorAutoConfiguration$$EnhancerBySpringCGLIB$$fee7de42",
		"resource": "null",
		"dependencies": ["management.health.status-org.springframework.boot.actuate.autoconfigure.HealthIndicatorProperties"]
	},
	{
		"bean": "healthAggregator",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.actuate.health.OrderedHealthAggregator",
		"resource": "class path resource [org/springframework/boot/actuate/autoconfigure/HealthIndicatorAutoConfiguration.class]",
		"dependencies": []
	},
	{
		"bean": "management.health.status-org.springframework.boot.actuate.autoconfigure.HealthIndicatorProperties",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.actuate.autoconfigure.HealthIndicatorProperties",
		"resource": "null",
		"dependencies": []
	},
	{
		"bean": "org.springframework.boot.actuate.autoconfigure.MetricRepositoryAutoConfiguration$FastMetricServicesConfiguration",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.actuate.autoconfigure.MetricRepositoryAutoConfiguration$FastMetricServicesConfiguration$$EnhancerBySpringCGLIB$$278d1dad",
		"resource": "null",
		"dependencies": []
	},
	{
		"bean": "counterBuffers",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.actuate.metrics.buffer.CounterBuffers",
		"resource": "class path resource [org/springframework/boot/actuate/autoconfigure/MetricRepositoryAutoConfiguration$FastMetricServicesConfiguration.class]",
		"dependencies": []
	},
	{
		"bean": "gaugeBuffers",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.actuate.metrics.buffer.GaugeBuffers",
		"resource": "class path resource [org/springframework/boot/actuate/autoconfigure/MetricRepositoryAutoConfiguration$FastMetricServicesConfiguration.class]",
		"dependencies": []
	},
	{
		"bean": "actuatorMetricReader",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.actuate.metrics.buffer.BufferMetricReader",
		"resource": "class path resource [org/springframework/boot/actuate/autoconfigure/MetricRepositoryAutoConfiguration$FastMetricServicesConfiguration.class]",
		"dependencies": ["counterBuffers",
		"gaugeBuffers"]
	},
	{
		"bean": "counterService",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.actuate.metrics.buffer.BufferCounterService",
		"resource": "class path resource [org/springframework/boot/actuate/autoconfigure/MetricRepositoryAutoConfiguration$FastMetricServicesConfiguration.class]",
		"dependencies": ["counterBuffers"]
	},
	{
		"bean": "gaugeService",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.actuate.metrics.buffer.BufferGaugeService",
		"resource": "class path resource [org/springframework/boot/actuate/autoconfigure/MetricRepositoryAutoConfiguration$FastMetricServicesConfiguration.class]",
		"dependencies": ["gaugeBuffers"]
	},
	{
		"bean": "org.springframework.boot.actuate.autoconfigure.MetricRepositoryAutoConfiguration",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.actuate.autoconfigure.MetricRepositoryAutoConfiguration$$EnhancerBySpringCGLIB$$5027ca05",
		"resource": "null",
		"dependencies": []
	},
	{
		"bean": "org.springframework.boot.autoconfigure.jmx.JmxAutoConfiguration",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.autoconfigure.jmx.JmxAutoConfiguration$$EnhancerBySpringCGLIB$$bf95287a",
		"resource": "null",
		"dependencies": []
	},
	{
		"bean": "mbeanExporter",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.jmx.export.annotation.AnnotationMBeanExporter",
		"resource": "class path resource [org/springframework/boot/autoconfigure/jmx/JmxAutoConfiguration.class]",
		"dependencies": ["objectNamingStrategy"]
	},
	{
		"bean": "objectNamingStrategy",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.autoconfigure.jmx.ParentAwareNamingStrategy",
		"resource": "class path resource [org/springframework/boot/autoconfigure/jmx/JmxAutoConfiguration.class]",
		"dependencies": []
	},
	{
		"bean": "mbeanServer",
		"aliases": [],
		"scope": "singleton",
		"type": "com.sun.jmx.mbeanserver.JmxMBeanServer",
		"resource": "class path resource [org/springframework/boot/autoconfigure/jmx/JmxAutoConfiguration.class]",
		"dependencies": []
	},
	{
		"bean": "org.springframework.boot.actuate.autoconfigure.PublicMetricsAutoConfiguration$TomcatMetricsConfiguration",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.actuate.autoconfigure.PublicMetricsAutoConfiguration$TomcatMetricsConfiguration$$EnhancerBySpringCGLIB$$5e1db386",
		"resource": "null",
		"dependencies": []
	},
	{
		"bean": "tomcatPublicMetrics",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.actuate.endpoint.TomcatPublicMetrics",
		"resource": "class path resource [org/springframework/boot/actuate/autoconfigure/PublicMetricsAutoConfiguration$TomcatMetricsConfiguration.class]",
		"dependencies": []
	},
	{
		"bean": "org.springframework.boot.actuate.autoconfigure.PublicMetricsAutoConfiguration$DataSourceMetricsConfiguration",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.actuate.autoconfigure.PublicMetricsAutoConfiguration$DataSourceMetricsConfiguration$$EnhancerBySpringCGLIB$$7b56c147",
		"resource": "null",
		"dependencies": []
	},
	{
		"bean": "dataSourcePublicMetrics",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.actuate.endpoint.DataSourcePublicMetrics",
		"resource": "class path resource [org/springframework/boot/actuate/autoconfigure/PublicMetricsAutoConfiguration$DataSourceMetricsConfiguration.class]",
		"dependencies": ["tomcatPoolDataSourceMetadataProvider"]
	},
	{
		"bean": "org.springframework.boot.actuate.autoconfigure.PublicMetricsAutoConfiguration",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.actuate.autoconfigure.PublicMetricsAutoConfiguration$$EnhancerBySpringCGLIB$$2251efb",
		"resource": "null",
		"dependencies": []
	},
	{
		"bean": "systemPublicMetrics",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.actuate.endpoint.SystemPublicMetrics",
		"resource": "class path resource [org/springframework/boot/actuate/autoconfigure/PublicMetricsAutoConfiguration.class]",
		"dependencies": []
	},
	{
		"bean": "metricReaderPublicMetrics",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.actuate.endpoint.MetricReaderPublicMetrics",
		"resource": "class path resource [org/springframework/boot/actuate/autoconfigure/PublicMetricsAutoConfiguration.class]",
		"dependencies": []
	},
	{
		"bean": "org.springframework.boot.actuate.autoconfigure.EndpointAutoConfiguration$RequestMappingEndpointConfiguration",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.actuate.autoconfigure.EndpointAutoConfiguration$RequestMappingEndpointConfiguration$$EnhancerBySpringCGLIB$$96d8e68",
		"resource": "null",
		"dependencies": []
	},
	{
		"bean": "requestMappingEndpoint",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.actuate.endpoint.RequestMappingEndpoint",
		"resource": "class path resource [org/springframework/boot/actuate/autoconfigure/EndpointAutoConfiguration$RequestMappingEndpointConfiguration.class]",
		"dependencies": []
	},
	{
		"bean": "org.springframework.boot.actuate.autoconfigure.EndpointAutoConfiguration",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.actuate.autoconfigure.EndpointAutoConfiguration$$EnhancerBySpringCGLIB$$4e32f38a",
		"resource": "null",
		"dependencies": []
	},
	{
		"bean": "environmentEndpoint",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.actuate.endpoint.EnvironmentEndpoint",
		"resource": "class path resource [org/springframework/boot/actuate/autoconfigure/EndpointAutoConfiguration.class]",
		"dependencies": []
	},
	{
		"bean": "healthEndpoint",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.actuate.endpoint.HealthEndpoint",
		"resource": "class path resource [org/springframework/boot/actuate/autoconfigure/EndpointAutoConfiguration.class]",
		"dependencies": []
	},
	{
		"bean": "beansEndpoint",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.actuate.endpoint.BeansEndpoint",
		"resource": "class path resource [org/springframework/boot/actuate/autoconfigure/EndpointAutoConfiguration.class]",
		"dependencies": []
	},
	{
		"bean": "infoEndpoint",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.actuate.endpoint.InfoEndpoint",
		"resource": "class path resource [org/springframework/boot/actuate/autoconfigure/EndpointAutoConfiguration.class]",
		"dependencies": []
	},
	{
		"bean": "metricsEndpoint",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.actuate.endpoint.MetricsEndpoint",
		"resource": "class path resource [org/springframework/boot/actuate/autoconfigure/EndpointAutoConfiguration.class]",
		"dependencies": []
	},
	{
		"bean": "traceEndpoint",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.actuate.endpoint.TraceEndpoint",
		"resource": "class path resource [org/springframework/boot/actuate/autoconfigure/EndpointAutoConfiguration.class]",
		"dependencies": []
	},
	{
		"bean": "dumpEndpoint",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.actuate.endpoint.DumpEndpoint",
		"resource": "class path resource [org/springframework/boot/actuate/autoconfigure/EndpointAutoConfiguration.class]",
		"dependencies": []
	},
	{
		"bean": "autoConfigurationReportEndpoint",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.actuate.endpoint.AutoConfigurationReportEndpoint",
		"resource": "class path resource [org/springframework/boot/actuate/autoconfigure/EndpointAutoConfiguration.class]",
		"dependencies": ["autoConfigurationReport"]
	},
	{
		"bean": "shutdownEndpoint",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.actuate.endpoint.ShutdownEndpoint",
		"resource": "class path resource [org/springframework/boot/actuate/autoconfigure/EndpointAutoConfiguration.class]",
		"dependencies": []
	},
	{
		"bean": "configurationPropertiesReportEndpoint",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.actuate.endpoint.ConfigurationPropertiesReportEndpoint",
		"resource": "class path resource [org/springframework/boot/actuate/autoconfigure/EndpointAutoConfiguration.class]",
		"dependencies": []
	},
	{
		"bean": "endpoints-org.springframework.boot.actuate.endpoint.EndpointProperties",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.actuate.endpoint.EndpointProperties",
		"resource": "null",
		"dependencies": []
	},
	{
		"bean": "org.springframework.boot.actuate.autoconfigure.EndpointMBeanExportAutoConfiguration",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.actuate.autoconfigure.EndpointMBeanExportAutoConfiguration$$EnhancerBySpringCGLIB$$29d3ebd9",
		"resource": "null",
		"dependencies": ["endpoints.jmx-org.springframework.boot.actuate.autoconfigure.EndpointMBeanExportProperties"]
	},
	{
		"bean": "endpointMBeanExporter",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.actuate.endpoint.jmx.EndpointMBeanExporter",
		"resource": "class path resource [org/springframework/boot/actuate/autoconfigure/EndpointMBeanExportAutoConfiguration.class]",
		"dependencies": ["mbeanServer"]
	},
	{
		"bean": "endpoints.jmx-org.springframework.boot.actuate.autoconfigure.EndpointMBeanExportProperties",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.actuate.autoconfigure.EndpointMBeanExportProperties",
		"resource": "null",
		"dependencies": []
	},
	{
		"bean": "org.springframework.boot.autoconfigure.web.ServerPropertiesAutoConfiguration",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.autoconfigure.web.ServerPropertiesAutoConfiguration$$EnhancerBySpringCGLIB$$f67f352e",
		"resource": "null",
		"dependencies": []
	},
	{
		"bean": "serverProperties",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.autoconfigure.web.ServerProperties",
		"resource": "class path resource [org/springframework/boot/autoconfigure/web/ServerPropertiesAutoConfiguration.class]",
		"dependencies": []
	},
	{
		"bean": "duplicateServerPropertiesDetector",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.autoconfigure.web.ServerPropertiesAutoConfiguration$DuplicateServerPropertiesDetector",
		"resource": "class path resource [org/springframework/boot/autoconfigure/web/ServerPropertiesAutoConfiguration.class]",
		"dependencies": []
	},
	{
		"bean": "org.springframework.boot.actuate.autoconfigure.ManagementServerPropertiesAutoConfiguration",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.actuate.autoconfigure.ManagementServerPropertiesAutoConfiguration$$EnhancerBySpringCGLIB$$28e40aa6",
		"resource": "null",
		"dependencies": []
	},
	{
		"bean": "managementServerProperties",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.actuate.autoconfigure.ManagementServerProperties",
		"resource": "class path resource [org/springframework/boot/actuate/autoconfigure/ManagementServerPropertiesAutoConfiguration.class]",
		"dependencies": []
	},
	{
		"bean": "org.springframework.boot.autoconfigure.web.HttpMessageConvertersAutoConfiguration$StringHttpMessageConverterConfiguration",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.autoconfigure.web.HttpMessageConvertersAutoConfiguration$StringHttpMessageConverterConfiguration$$EnhancerBySpringCGLIB$$8d57e25e",
		"resource": "null",
		"dependencies": ["spring.http.encoding-org.springframework.boot.autoconfigure.web.HttpEncodingProperties"]
	},
	{
		"bean": "stringHttpMessageConverter",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.http.converter.StringHttpMessageConverter",
		"resource": "class path resource [org/springframework/boot/autoconfigure/web/HttpMessageConvertersAutoConfiguration$StringHttpMessageConverterConfiguration.class]",
		"dependencies": []
	},
	{
		"bean": "spring.http.encoding-org.springframework.boot.autoconfigure.web.HttpEncodingProperties",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.autoconfigure.web.HttpEncodingProperties",
		"resource": "null",
		"dependencies": []
	},
	{
		"bean": "org.springframework.boot.autoconfigure.web.JacksonHttpMessageConvertersConfiguration$MappingJackson2HttpMessageConverterConfiguration",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.autoconfigure.web.JacksonHttpMessageConvertersConfiguration$MappingJackson2HttpMessageConverterConfiguration$$EnhancerBySpringCGLIB$$1b660c5e",
		"resource": "null",
		"dependencies": []
	},
	{
		"bean": "mappingJackson2HttpMessageConverter",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.http.converter.json.MappingJackson2HttpMessageConverter",
		"resource": "class path resource [org/springframework/boot/autoconfigure/web/JacksonHttpMessageConvertersConfiguration$MappingJackson2HttpMessageConverterConfiguration.class]",
		"dependencies": ["jacksonObjectMapper"]
	},
	{
		"bean": "org.springframework.boot.autoconfigure.web.JacksonHttpMessageConvertersConfiguration",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.autoconfigure.web.JacksonHttpMessageConvertersConfiguration$$EnhancerBySpringCGLIB$$ae53a4d4",
		"resource": "null",
		"dependencies": []
	},
	{
		"bean": "org.springframework.boot.autoconfigure.web.HttpMessageConvertersAutoConfiguration",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.autoconfigure.web.HttpMessageConvertersAutoConfiguration$$EnhancerBySpringCGLIB$$d0e1d7be",
		"resource": "null",
		"dependencies": []
	},
	{
		"bean": "messageConverters",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.autoconfigure.web.HttpMessageConverters",
		"resource": "class path resource [org/springframework/boot/autoconfigure/web/HttpMessageConvertersAutoConfiguration.class]",
		"dependencies": []
	},
	{
		"bean": "org.springframework.boot.actuate.autoconfigure.EndpointWebMvcManagementContextConfiguration",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.actuate.autoconfigure.EndpointWebMvcManagementContextConfiguration$$EnhancerBySpringCGLIB$$1dfdcb53",
		"resource": "null",
		"dependencies": ["endpoints.health-org.springframework.boot.actuate.autoconfigure.HealthMvcEndpointProperties",
		"managementServerProperties",
		"endpoints.cors-org.springframework.boot.actuate.autoconfigure.EndpointCorsProperties"]
	},
	{
		"bean": "endpointHandlerMapping",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.actuate.endpoint.mvc.EndpointHandlerMapping",
		"resource": "class path resource [org/springframework/boot/actuate/autoconfigure/EndpointWebMvcManagementContextConfiguration.class]",
		"dependencies": []
	},
	{
		"bean": "mvcEndpoints",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.actuate.endpoint.mvc.MvcEndpoints",
		"resource": "class path resource [org/springframework/boot/actuate/autoconfigure/EndpointWebMvcManagementContextConfiguration.class]",
		"dependencies": []
	},
	{
		"bean": "environmentMvcEndpoint",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.actuate.endpoint.mvc.EnvironmentMvcEndpoint",
		"resource": "class path resource [org/springframework/boot/actuate/autoconfigure/EndpointWebMvcManagementContextConfiguration.class]",
		"dependencies": ["environmentEndpoint"]
	},
	{
		"bean": "heapdumpMvcEndpoint",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.actuate.endpoint.mvc.HeapdumpMvcEndpoint",
		"resource": "class path resource [org/springframework/boot/actuate/autoconfigure/EndpointWebMvcManagementContextConfiguration.class]",
		"dependencies": []
	},
	{
		"bean": "healthMvcEndpoint",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.actuate.endpoint.mvc.HealthMvcEndpoint",
		"resource": "class path resource [org/springframework/boot/actuate/autoconfigure/EndpointWebMvcManagementContextConfiguration.class]",
		"dependencies": ["healthEndpoint"]
	},
	{
		"bean": "metricsMvcEndpoint",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.actuate.endpoint.mvc.MetricsMvcEndpoint",
		"resource": "class path resource [org/springframework/boot/actuate/autoconfigure/EndpointWebMvcManagementContextConfiguration.class]",
		"dependencies": ["metricsEndpoint"]
	},
	{
		"bean": "endpoints.health-org.springframework.boot.actuate.autoconfigure.HealthMvcEndpointProperties",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.actuate.autoconfigure.HealthMvcEndpointProperties",
		"resource": "null",
		"dependencies": []
	},
	{
		"bean": "endpoints.cors-org.springframework.boot.actuate.autoconfigure.EndpointCorsProperties",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.actuate.autoconfigure.EndpointCorsProperties",
		"resource": "null",
		"dependencies": []
	},
	{
		"bean": "org.springframework.boot.actuate.autoconfigure.EndpointWebMvcAutoConfiguration$EndpointWebMvcConfiguration",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.actuate.autoconfigure.EndpointWebMvcAutoConfiguration$EndpointWebMvcConfiguration$$EnhancerBySpringCGLIB$$282da9fb",
		"resource": "null",
		"dependencies": []
	},
	{
		"bean": "org.springframework.boot.actuate.autoconfigure.EndpointWebMvcAutoConfiguration$ApplicationContextFilterConfiguration",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.actuate.autoconfigure.EndpointWebMvcAutoConfiguration$ApplicationContextFilterConfiguration$$EnhancerBySpringCGLIB$$94b786ff",
		"resource": "null",
		"dependencies": []
	},
	{
		"bean": "applicationContextIdFilter",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.web.filter.ApplicationContextHeaderFilter",
		"resource": "class path resource [org/springframework/boot/actuate/autoconfigure/EndpointWebMvcAutoConfiguration$ApplicationContextFilterConfiguration.class]",
		"dependencies": ["org.springframework.boot.context.embedded.AnnotationConfigEmbeddedWebApplicationContext@27d14185"]
	},
	{
		"bean": "org.springframework.boot.actuate.autoconfigure.EndpointWebMvcAutoConfiguration",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.actuate.autoconfigure.EndpointWebMvcAutoConfiguration$$EnhancerBySpringCGLIB$$f2cb8584",
		"resource": "null",
		"dependencies": []
	},
	{
		"bean": "managementContextResolver",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.actuate.autoconfigure.ManagementContextResolver",
		"resource": "class path resource [org/springframework/boot/actuate/autoconfigure/EndpointWebMvcAutoConfiguration.class]",
		"dependencies": []
	},
	{
		"bean": "managementServletContext",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.actuate.autoconfigure.EndpointWebMvcAutoConfiguration$1",
		"resource": "class path resource [org/springframework/boot/actuate/autoconfigure/EndpointWebMvcAutoConfiguration.class]",
		"dependencies": ["managementServerProperties"]
	},
	{
		"bean": "org.springframework.boot.actuate.autoconfigure.MetricExportAutoConfiguration$MetricExportPropertiesConfiguration",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.actuate.autoconfigure.MetricExportAutoConfiguration$MetricExportPropertiesConfiguration$$EnhancerBySpringCGLIB$$3023dc16",
		"resource": "null",
		"dependencies": []
	},
	{
		"bean": "spring.metrics.export-org.springframework.boot.actuate.metrics.export.MetricExportProperties",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.actuate.metrics.export.MetricExportProperties",
		"resource": "class path resource [org/springframework/boot/actuate/autoconfigure/MetricExportAutoConfiguration$MetricExportPropertiesConfiguration.class]",
		"dependencies": []
	},
	{
		"bean": "org.springframework.boot.actuate.autoconfigure.MetricExportAutoConfiguration$StatsdConfiguration",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.actuate.autoconfigure.MetricExportAutoConfiguration$StatsdConfiguration$$EnhancerBySpringCGLIB$$85d38d48",
		"resource": "null",
		"dependencies": []
	},
	{
		"bean": "org.springframework.boot.actuate.autoconfigure.MetricExportAutoConfiguration",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.actuate.autoconfigure.MetricExportAutoConfiguration$$EnhancerBySpringCGLIB$$8812fa1b",
		"resource": "null",
		"dependencies": ["spring.metrics.export-org.springframework.boot.actuate.metrics.export.MetricExportProperties"]
	},
	{
		"bean": "metricWritersMetricExporter",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.actuate.metrics.export.MetricExporters",
		"resource": "class path resource [org/springframework/boot/actuate/autoconfigure/MetricExportAutoConfiguration.class]",
		"dependencies": ["spring.metrics.export-org.springframework.boot.actuate.metrics.export.MetricExportProperties"]
	},
	{
		"bean": "org.springframework.boot.actuate.autoconfigure.MetricFilterAutoConfiguration",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.actuate.autoconfigure.MetricFilterAutoConfiguration$$EnhancerBySpringCGLIB$$5c7a0e57",
		"resource": "null",
		"dependencies": ["counterService",
		"gaugeService",
		"endpoints.metrics.filter-org.springframework.boot.actuate.autoconfigure.MetricFilterProperties"]
	},
	{
		"bean": "metricsFilter",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.actuate.autoconfigure.MetricsFilter",
		"resource": "class path resource [org/springframework/boot/actuate/autoconfigure/MetricFilterAutoConfiguration.class]",
		"dependencies": []
	},
	{
		"bean": "endpoints.metrics.filter-org.springframework.boot.actuate.autoconfigure.MetricFilterProperties",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.actuate.autoconfigure.MetricFilterProperties",
		"resource": "null",
		"dependencies": []
	},
	{
		"bean": "org.springframework.boot.actuate.autoconfigure.TraceRepositoryAutoConfiguration",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.actuate.autoconfigure.TraceRepositoryAutoConfiguration$$EnhancerBySpringCGLIB$$95769ee6",
		"resource": "null",
		"dependencies": []
	},
	{
		"bean": "traceRepository",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.actuate.trace.InMemoryTraceRepository",
		"resource": "class path resource [org/springframework/boot/actuate/autoconfigure/TraceRepositoryAutoConfiguration.class]",
		"dependencies": []
	},
	{
		"bean": "org.springframework.boot.actuate.autoconfigure.TraceWebFilterAutoConfiguration",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.actuate.autoconfigure.TraceWebFilterAutoConfiguration$$EnhancerBySpringCGLIB$$3891e338",
		"resource": "null",
		"dependencies": ["traceRepository",
		"management.trace-org.springframework.boot.actuate.trace.TraceProperties"]
	},
	{
		"bean": "webRequestLoggingFilter",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.actuate.trace.WebRequestTraceFilter",
		"resource": "class path resource [org/springframework/boot/actuate/autoconfigure/TraceWebFilterAutoConfiguration.class]",
		"dependencies": ["org.springframework.beans.factory.support.DefaultListableBeanFactory@21f58f66"]
	},
	{
		"bean": "management.trace-org.springframework.boot.actuate.trace.TraceProperties",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.actuate.trace.TraceProperties",
		"resource": "null",
		"dependencies": []
	},
	{
		"bean": "org.springframework.boot.autoconfigure.aop.AopAutoConfiguration$JdkDynamicAutoProxyConfiguration",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.autoconfigure.aop.AopAutoConfiguration$JdkDynamicAutoProxyConfiguration$$EnhancerBySpringCGLIB$$cf9b00cf",
		"resource": "null",
		"dependencies": []
	},
	{
		"bean": "org.springframework.boot.autoconfigure.aop.AopAutoConfiguration",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.autoconfigure.aop.AopAutoConfiguration$$EnhancerBySpringCGLIB$$8b803820",
		"resource": "null",
		"dependencies": []
	},
	{
		"bean": "org.springframework.boot.autoconfigure.context.ConfigurationPropertiesAutoConfiguration",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.autoconfigure.context.ConfigurationPropertiesAutoConfiguration$$EnhancerBySpringCGLIB$$2fb344ac",
		"resource": "null",
		"dependencies": []
	},
	{
		"bean": "org.springframework.boot.autoconfigure.dao.PersistenceExceptionTranslationAutoConfiguration",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.autoconfigure.dao.PersistenceExceptionTranslationAutoConfiguration",
		"resource": "null",
		"dependencies": []
	},
	{
		"bean": "persistenceExceptionTranslationPostProcessor",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.dao.annotation.PersistenceExceptionTranslationPostProcessor",
		"resource": "class path resource [org/springframework/boot/autoconfigure/dao/PersistenceExceptionTranslationAutoConfiguration.class]",
		"dependencies": []
	},
	{
		"bean": "org.springframework.boot.autoconfigure.data.jpa.JpaRepositoriesAutoConfiguration",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.autoconfigure.data.jpa.JpaRepositoriesAutoConfiguration$$EnhancerBySpringCGLIB$$f004a712",
		"resource": "null",
		"dependencies": []
	},
	{
		"bean": "org.springframework.data.repository.core.support.RepositoryFactoryBeanSupport_Predictor",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.data.repository.core.support.FactoryBeanTypePredictingBeanPostProcessor",
		"resource": "null",
		"dependencies": []
	},
	{
		"bean": "emBeanDefinitionRegistrarPostProcessor",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.data.jpa.repository.support.EntityManagerBeanDefinitionRegistrarPostProcessor",
		"resource": "null",
		"dependencies": []
	},
	{
		"bean": "jpaMappingContext",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.data.jpa.mapping.JpaMetamodelMappingContext",
		"resource": "null",
		"dependencies": []
	},
	{
		"bean": "jpaContext",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.data.jpa.repository.support.DefaultJpaContext",
		"resource": "null",
		"dependencies": ["org.springframework.orm.jpa.SharedEntityManagerCreator#0"]
	},
	{
		"bean": "userRepository",
		"aliases": [],
		"scope": "singleton",
		"type": "com.hellojd.cloud.repository.UserRepository",
		"resource": "null",
		"dependencies": ["(inner bean)#7a272b1e",
		"(inner bean)#498ea4a1",
		"(inner bean)#460a9b36",
		"jpaMappingContext"]
	},
	{
		"bean": "org.springframework.data.web.config.SpringDataWebConfiguration",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.data.web.config.SpringDataWebConfiguration$$EnhancerBySpringCGLIB$$a18de7b1",
		"resource": "null",
		"dependencies": []
	},
	{
		"bean": "pageableResolver",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.data.web.PageableHandlerMethodArgumentResolver",
		"resource": "class path resource [org/springframework/data/web/config/SpringDataWebConfiguration.class]",
		"dependencies": []
	},
	{
		"bean": "sortResolver",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.data.web.SortHandlerMethodArgumentResolver",
		"resource": "class path resource [org/springframework/data/web/config/SpringDataWebConfiguration.class]",
		"dependencies": []
	},
	{
		"bean": "org.springframework.data.web.config.SpringDataJacksonConfiguration",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.data.web.config.SpringDataJacksonConfiguration$$EnhancerBySpringCGLIB$$78d02d32",
		"resource": "null",
		"dependencies": []
	},
	{
		"bean": "jacksonGeoModule",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.data.geo.GeoModule",
		"resource": "class path resource [org/springframework/data/web/config/SpringDataJacksonConfiguration.class]",
		"dependencies": []
	},
	{
		"bean": "org.springframework.boot.autoconfigure.data.web.SpringDataWebAutoConfiguration",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.autoconfigure.data.web.SpringDataWebAutoConfiguration$$EnhancerBySpringCGLIB$$2bc06f7f",
		"resource": "null",
		"dependencies": []
	},
	{
		"bean": "org.springframework.transaction.annotation.ProxyTransactionManagementConfiguration",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.transaction.annotation.ProxyTransactionManagementConfiguration$$EnhancerBySpringCGLIB$$4029b95e",
		"resource": "null",
		"dependencies": []
	},
	{
		"bean": "org.springframework.boot.autoconfigure.jdbc.DataSourceTransactionManagerAutoConfiguration$TransactionManagementConfiguration",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.autoconfigure.jdbc.DataSourceTransactionManagerAutoConfiguration$TransactionManagementConfiguration$$EnhancerBySpringCGLIB$$b6017a70",
		"resource": "null",
		"dependencies": []
	},
	{
		"bean": "org.springframework.boot.autoconfigure.jdbc.DataSourceTransactionManagerAutoConfiguration$DataSourceTransactionManagerConfiguration",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.autoconfigure.jdbc.DataSourceTransactionManagerAutoConfiguration$DataSourceTransactionManagerConfiguration$$EnhancerBySpringCGLIB$$ed2a51cd",
		"resource": "null",
		"dependencies": ["dataSource"]
	},
	{
		"bean": "org.springframework.boot.autoconfigure.jdbc.DataSourceTransactionManagerAutoConfiguration",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.autoconfigure.jdbc.DataSourceTransactionManagerAutoConfiguration$$EnhancerBySpringCGLIB$$5100a9af",
		"resource": "null",
		"dependencies": []
	},
	{
		"bean": "org.springframework.boot.autoconfigure.jdbc.JdbcTemplateAutoConfiguration",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.autoconfigure.jdbc.JdbcTemplateAutoConfiguration$$EnhancerBySpringCGLIB$$600dee4e",
		"resource": "null",
		"dependencies": ["dataSource"]
	},
	{
		"bean": "jdbcTemplate",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.jdbc.core.JdbcTemplate",
		"resource": "class path resource [org/springframework/boot/autoconfigure/jdbc/JdbcTemplateAutoConfiguration.class]",
		"dependencies": []
	},
	{
		"bean": "namedParameterJdbcTemplate",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.jdbc.core.namedparam.NamedParameterJdbcTemplate",
		"resource": "class path resource [org/springframework/boot/autoconfigure/jdbc/JdbcTemplateAutoConfiguration.class]",
		"dependencies": []
	},
	{
		"bean": "org.springframework.boot.autoconfigure.transaction.TransactionAutoConfiguration",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.autoconfigure.transaction.TransactionAutoConfiguration$$EnhancerBySpringCGLIB$$d49db468",
		"resource": "null",
		"dependencies": ["transactionManager"]
	},
	{
		"bean": "transactionTemplate",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.transaction.support.TransactionTemplate",
		"resource": "class path resource [org/springframework/boot/autoconfigure/transaction/TransactionAutoConfiguration.class]",
		"dependencies": []
	},
	{
		"bean": "org.springframework.boot.autoconfigure.web.HttpEncodingAutoConfiguration",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.autoconfigure.web.HttpEncodingAutoConfiguration$$EnhancerBySpringCGLIB$$17162009",
		"resource": "null",
		"dependencies": ["spring.http.encoding-org.springframework.boot.autoconfigure.web.HttpEncodingProperties"]
	},
	{
		"bean": "characterEncodingFilter",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.web.filter.OrderedCharacterEncodingFilter",
		"resource": "class path resource [org/springframework/boot/autoconfigure/web/HttpEncodingAutoConfiguration.class]",
		"dependencies": []
	},
	{
		"bean": "localeCharsetMappingsCustomizer",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.autoconfigure.web.HttpEncodingAutoConfiguration$LocaleCharsetMappingsCustomizer",
		"resource": "class path resource [org/springframework/boot/autoconfigure/web/HttpEncodingAutoConfiguration.class]",
		"dependencies": []
	},
	{
		"bean": "org.springframework.boot.autoconfigure.web.MultipartAutoConfiguration",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.autoconfigure.web.MultipartAutoConfiguration$$EnhancerBySpringCGLIB$$fad76ca4",
		"resource": "null",
		"dependencies": ["spring.http.multipart-org.springframework.boot.autoconfigure.web.MultipartProperties"]
	},
	{
		"bean": "multipartConfigElement",
		"aliases": [],
		"scope": "singleton",
		"type": "javax.servlet.MultipartConfigElement",
		"resource": "class path resource [org/springframework/boot/autoconfigure/web/MultipartAutoConfiguration.class]",
		"dependencies": []
	},
	{
		"bean": "multipartResolver",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.web.multipart.support.StandardServletMultipartResolver",
		"resource": "class path resource [org/springframework/boot/autoconfigure/web/MultipartAutoConfiguration.class]",
		"dependencies": []
	},
	{
		"bean": "spring.http.multipart-org.springframework.boot.autoconfigure.web.MultipartProperties",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.autoconfigure.web.MultipartProperties",
		"resource": "null",
		"dependencies": []
	},
	{
		"bean": "org.springframework.boot.autoconfigure.web.WebClientAutoConfiguration$RestTemplateConfiguration",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.autoconfigure.web.WebClientAutoConfiguration$RestTemplateConfiguration$$EnhancerBySpringCGLIB$$47593075",
		"resource": "null",
		"dependencies": []
	},
	{
		"bean": "restTemplateBuilder",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.web.client.RestTemplateBuilder",
		"resource": "class path resource [org/springframework/boot/autoconfigure/web/WebClientAutoConfiguration$RestTemplateConfiguration.class]",
		"dependencies": []
	},
	{
		"bean": "org.springframework.boot.autoconfigure.web.WebClientAutoConfiguration",
		"aliases": [],
		"scope": "singleton",
		"type": "org.springframework.boot.autoconfigure.web.WebClientAutoConfiguration$$EnhancerBySpringCGLIB$$50c8de11",
		"resource": "null",
		"dependencies": []
	},
	{
		"bean": "org.springframework.orm.jpa.SharedEntityManagerCreator#0",
		"aliases": [],
		"scope": "singleton",
		"type": "com.sun.proxy.$Proxy105",
		"resource": "null",
		"dependencies": ["entityManagerFactory"]
	}]
}]