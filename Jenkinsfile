 node {
 

 stage("configure") {
     
     bat script: $/ mkdir  $WORKSPACE\$BUILD_NUMBER /$

    }

 

 stage('run test'){
     
     bat script: $/ mkdir \tmp\reports /$
     
     bat script: $/ cd C:\Users\Olga_Velikaya\Documents\Performance\apache-jmeter-5.5\apache-jmeter-5.5\bin" /$
     
     bat script: $/ jmeter -Jjmeter.save.saveservice.output_format=csv -n -t C:\Users\Olga_Velikaya\Documents\Performance\apache-jmeter-5.5\apache-jmeter-5.5\oavelika_testplan.jmx -l \tmp\reports\JMeter.jtl -e -o \tmp\reports\HtmlReport /$
     
     
 }

 

 stage('publish results'){
     
     bat script: $/ move \tmp\reports\* $WORKSPACE\$BUILD_NUMBER /$
     
     archiveArtifacts artifacts:  $/ **/*.jtl, $WORKSPACE\$BUILD_NUMBER\HtmlReport\index.html /$
     
     } 
}
  
