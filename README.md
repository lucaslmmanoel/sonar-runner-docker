# sonnar-runner-docker
Criando uma imagem docker para rodar o sonar runner


# Para Executar O sonnar runner em seu projeto basta criar um arquivo chamado
# sonar-runner.properties contendo o token a linguagem e etc



## Com o arquivo criado só executar este comando na pasta do projeto

	docker run --entrypoint /opt/sonar-runner-2.4/bin/sonar-runner \
	-e SONAR_USER_HOME=/data/.sonar-cache \
	-v `pwd`:/data -u `id -u` lucaslmmanoel/sonnar-runner -X  \
		-Dsonar.host.url=https://yoursonar.instance.com.br \
