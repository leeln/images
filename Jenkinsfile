node {
  stage 'package'
 
  docker.withRegistry('https://docker.repo.leeln.com','leeln-admin') {
  	checkout scm
  	docker.build('leeln/base:alpine', 'base/alpine').push()

  	docker.build('leeln/java:jdk-7', 'java/7/jdk').push()
  	docker.build('leeln/java:jre-7', 'java/7/jre').push()

  	docker.build('leeln/java:jdk-8', 'java/8/jdk').push()
  	docker.build('leeln/java:jre-8', 'java/8/jre').push()
  }
}