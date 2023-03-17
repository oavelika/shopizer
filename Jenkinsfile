  node {
 

 stage("configure") {

        sh "mkdir C:/\\Users/\\Olga_Velikaya/\\.jenkins/\\workspace/\\jmeter_pipeline/\\$BUILD_NUMBER/\\"

    }

 

 stage('run test'){

 sh "mkdir -p /\\tmp/\\reports"

 sh "cd C:/\\Users/\\Olga_Velikaya/\\Documents/\\Performance/\\apache-jmeter-5.5/\\apache-jmeter-5.5/\\bin"

      sh """jmeterw.cmd -Jjmeter.save.saveservice.output_format=xml

          -n -t app/\\C:/\\Users/\\Olga_Velikaya/\\Documents/\\Performance/\\apache-jmeter-5.5/\\apache-jmeter-5.5/\\oavelika_testplan.jmx

            -l /\\tmp/\\reports/\\JMeter.jtl -e -o /\\tmp/\\reports/\\HtmlReport"""

 }

 

 stage('publish results'){

 sh "mv /\\tmp/\\reports/\\* C:/\\Users/\\Olga_Velikaya/\\.jenkins/\\workspace/\\jmeter_pipeline/\\$BUILD_NUMBER/\\"

 archiveArtifacts artifacts: 'C:/\\Users/\\Olga_Velikaya/\\.jenkins/\\workspace/\\jmeter_pipeline/\\$BUILD_NUMBER/\\JMeter.jtl, C:/\\Users/\\Olga_Velikaya/\\.jenkins/\\workspace/\\jmeter_pipeline/\\$BUILD_NUMBER/\\HtmlReport/\\index.html'

    } 

  }
