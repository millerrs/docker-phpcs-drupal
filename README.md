# PHP_CodeSniffer for Drupal
A PHP_CodeSniffer image for checking Drupal code compliance.

## Usage

```bash
docker run -it --rm -v /path/to/code:/app millerrs/phpcs-drupal
```

## Usage in Jenkins Pipeline

```groovy
stage('Check Drupal Code Compliance') {
    agent {
        docker {
            image 'millerrs/phpcs-drupal'
        }
    }
    steps {
        sh 'phpcs --standard=Drupal,DrupalPractice web/modules/custom'
    }
}
```
