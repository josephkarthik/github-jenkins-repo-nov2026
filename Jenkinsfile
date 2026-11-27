pipeline{ 
    agent any 
    tools{
        maven 'mymaven'
    }
    stages{
        stage('get the code from github'){
            steps{
                git 'https://github.com/josephkarthik/DevOpsCodeDemo.git'
            }

        }
        stage('code review'){
            steps{
                sh "mvn pmd:pmd"
            }
        }
        stage('compile the code'){
            steps{
                sh "mvn compile"
            }
        }
        stage('package the code'){
            steps{
                sh "mvn package"
            }
        }
    }
}
// apt remove openjdk-17-jre-headless -y to remove java version
//if you are writing pipeline script in visual studio install JENKINS PIPELINE LINTER CONNECTOR AND JENKINS FILE SUPPORT TO MAKE USE OF CORRECTING THE CODE BY DEFAULT 
//TABNINE ai code generator, it installs by default ,if not please install. now it is not free, it is paid tool
//go to tools in jenkins and click on add maven and save it and it will install maven by default when you run project
//go to Available plugins and install pipeline stage view plugin
// Also install warnings plugin
//to generate pipeline script by default
//click on generate pipeline syntax script, when you scroll down you will find this option in the last 
//and in sample step select record issues: record compiler warnings and static analysis results
//and in tools section select PMD
//and in Report File Pattern copy and paste **/pmd.xml
//click and generate pipelie script 
//copy the script and paste in sucess block of pipeline script :: recordIssues sourceCodeRetention: 'LAST_BUILD', tools: [pmdParser(pattern: '**/pmd.xml')]
//copy the above code and paste it in sucess block
//now again generate one more script , click on pipeline syntax again
//select junit archive junit formated test results
//type this in test reports xml block: target/surefire-reports/*.xml 
// above line means , i want to take all the xml files and generate test report
//click on generate pipeline script you will get code: junit 'target/surefire-reports/*.xml' // dont paste this , it is for knowledge purpose only, by default this will be there in the script
//paste this code junit 'target/surefire-reports/*.xml' in test block of pipeline script
