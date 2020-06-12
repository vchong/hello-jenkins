http://code.tutsplus.com/tutorials/setting-up-continuous-integration-continuous-deployment-with-jenkins--cms-21511

dev machine = mac
app = victor, IE use usr=victor stead o usr=app!!!
admin = victor, IE use usr=victor stead o usr=admin!!!
app server = linbuntu @ port 80, app @ /home/victor/work/nobckup/bb/jenkins/hello-jenkins
jenkins-box = linbuntu @ port 8080, usr jenkins' $HOME @ /var/lib/jenkins
git server = linbuntu, repos @ /home/victor/work/nobckup/bb/jenkins/git_server_repos

f mac, stead o setting PORT=80 in /etc/environment which does NOT xist
just do 'export PORT=80'
running an app on port 80 requires root privileges
n sudo setcap cap_net_bind_service=+ep /usr/local/bin/node
does NOT work since setcap is NOT a cmd in mac
so u either 'node app.js' s root
or use port 5000

#see job's console output f err msg
#y script/test not executable when git fetched fr jenkins?
 #hv 2 'chmod a+x' in build steps s workard
#copied 'node' fr /home/victor/bin to /usr/local/bin cos /home/victor/bin not in jenkins PATH as read fr /usr/bin/env
