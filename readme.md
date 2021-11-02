# Projeto Java com Gradle
## O Gradle é um sistema de automação de compilação de código. E Gerenciamento de dependencias.



Alguns comandos básicos do Gradle e suas finalidades.



gradle run - Executa nosso projeto e cria a pasta Build



Criando uma task

task nameTask{

​	group MyGroup

​	description "essa é uma task de teste"	

​	doFirst{

​			println "Será executado primeiro"

​	}

​	doLast{

​			println "Será executado no Final"

​	}

}







Alguns comandos de dependência entre as tasks:

finalizedBy - define uma outra task para ser executada ao finalizar a execução da task em questão.

dependsOn - Define se a task só pode ser executada caso a task referenciada tenha sido executada antes. Ele força e executa a task antes da nossa.

mustRunAfter - Quando são executadas duas tasks ao mesmo tempo, esse comando define que essa será executada somente após a task referenciada. Mesmo que essas tasks possam ser executadas individualmente. Somente quando executadas juntas que esse comando é obedecido.

