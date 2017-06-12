ansiColor('xterm') {
  node('docker') {
     git "https://github.com/juliogonzalez/poppler-amazon-rpm.git"
  }

  stage("Tests") {
    parallel(
      "amazon2016.09": {
        node('docker') {
          checkout scm
          sh "./ci --notty --remove-on-error --distro=amazon2016.09"
        }  
      },
      "amazon2017.03": {
        node('docker') {
          checkout scm
          sh "./ci --notty --remove-on-error --distro=amazon2017.03"
        }
      }
    )
  }
}
