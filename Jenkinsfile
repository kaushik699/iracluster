//jenkinsfile
pipeline {
  agent any

  environment {
    DOCKER_HUB_CREDS = credentials('dockerhub-creds') 
    DOCKERHUB_USER = "${DOCKER_HUB_CREDS_USR}"
    DOCKERHUB_PASS = "${DOCKER_HUB_CREDS_PSW}"
    IMAGE_TAG = "${BUILD_NUMBER}"
  }

  stages {

    stage('Checkout') {
      steps {
        checkout scm
      }
    }

    stage('Build Docker Images') {
      steps {
        script {
          sh "docker build -t ${DOCKERHUB_USER}/irapass:${IMAGE_TAG} ./irapass"
          sh "docker build -t ${DOCKERHUB_USER}/irapodtracker:${IMAGE_TAG} ./irapodtracker"
          sh "docker build -t ${DOCKERHUB_USER}/irapodwatcher:${IMAGE_TAG} ./irapodwatcher"
        }
      }
    }

    stage('Login to Docker Hub') {
      steps {
        script {
          sh "echo ${DOCKERHUB_PASS} | docker login -u ${DOCKERHUB_USER} --password-stdin"
        }
      }
    }

    stage('Push Docker Images') {
      steps {
        script {
          sh "docker push ${DOCKERHUB_USER}/irapass:${IMAGE_TAG}"
          sh "docker push ${DOCKERHUB_USER}/irapodtracker:${IMAGE_TAG}"
          sh "docker push ${DOCKERHUB_USER}/irapodwatcher:${IMAGE_TAG}"
        }
      }
    }

  }

  post {
    always {
      cleanWs()
    }
  }
}
