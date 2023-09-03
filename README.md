# car-api-project
Forking for demo testing

Testing -1
Testing -2
Testing -3
Testing -4

Groovy Script:-

pipeline{
agent any
stages{
stage("checkout by akshat"){
steps{
git url: 'https://github.com/akshu20791/DevOpsClassCodes'
}
}
stage("codecompile with akshat"){
steps{
sh "mvn compile"
}
}
stage("codetesting with akshat"){
steps{
sh "mvn test"
}

}
stage("codeqa with akshat"){
steps{
sh "mvn pmd:pmd"
}
}
stage("package"){
steps{
sh "mvn package"
}
}
}

}
