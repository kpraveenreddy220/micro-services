#Zuul 

Zuul is an L7 application gateway that provides capabilities for dynamic routing, monitoring, resiliency, security, and more. Please view the wiki for usage, information, HOWTO, etc https://github.com/Netflix/zuul/wiki

## Example URI 
* When currency-exchange-service instance is being invoked, it has to go through Zuul gateway API for authentication or authorization or logging purposes. 

	Syntax: 	http://localhost:8765/{project or service name }/{URI}
	EX: 		http://localhost:8765/currency-exchange-service/currency-exchange/from/EUR/to/INR
	
## Communications between curreny-converter-service and Currency-exchange-service through Zuul

	Syntax: 	http://localhost:8765/{project or service name}/{URI}
	Ex: 		http://localhost:8765/currency-converter-service/currency-converter-feign/from/USD/to/INR/quantity/28
	
	
## To start Zipkin connected to RabbitMQ
	RABBIT_ADDRESSES=localhost java -jar zipkin.jar
	
## To Start RabbitMQ server via Homebrew 
	brew update
	brew install rabbitmq
	export PATH=$PATH:/usr/local/opt/rabbitmq/sbin
	rabbitmq-server

