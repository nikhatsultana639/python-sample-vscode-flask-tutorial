pipeline 
{
agent { label 'built-in' }
stages
{
stage('clone from git')
{
steps
{
git branch: 'main', url: 'https://github.com/nikhatsultana639/python-sample-vscode-flask-tutorial.git'
}
}
stage('installing dependencies')
{
steps
{
sh "pip install flake8"
sh "pip install pytest"
}
}
stage('test')
{
steps
{
sh "pytest"
 }
 }
 stage('test wtih flake')
 {
 steps
 {
 sh "flake8 ."
 }
 }  
 }
 }
