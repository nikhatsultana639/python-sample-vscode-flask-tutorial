pipeline 
{
agent { label 'built-in' }
stages
{
stage('clone from git')
{
steps
{
git branch: 'master', url: 'https://github.com/nikhatsultana639/python-sample-vscode-flask-tutorial.git'
}
}
stage('installing dependencies')
{
steps
{
sh "pip install flake8"
sh "pip install pytest"
sh "python3 -m pip install --upgrade pip setuptools wheel"
sh "pip install -r requirements.txt"
sh "pip install pytest-cov"
}
}
stage('test')
{
steps
{
sh "pytest"
sh "pytest --doctest-modules --junitxml=junit/test-results.xml --cov=. --cov-report=xml"
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
