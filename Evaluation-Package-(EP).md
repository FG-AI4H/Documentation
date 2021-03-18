# Scope
Here we track all changes and tasks necessary to bring the EvalAI platform to life.
Staging frontend is at https://3.64.132.163/ (due to the self-signed SSL, browsers give a warning)

# "Off-line" Tasks
(stuff that needs to be done outside of the repo or AWS account)
- get domain
- get signed ssl certificate
- register with email service

# Tasks
| Task | Description and Purpose | Responsible | Status |
|--|--|--|--|
| Move Repo to Github | Switch origin in respective folder on AWS instances and also adapt the "download secrets from S3" mechanism | Steffen | [ ] |
| Check Access Policy from EC2 to S3| Worker needs to be able to read the .zip; Currently there is a 403 error | Dominik | [ ] |
(SV): I still need to move the rest of the tasks to this list

# Changes as part of troubleshooting

List from Steffen
- /media/ in S3 is pulled with AWS CLI rather the official django migrate command (there was an error; see line 8:9 in /docker/prod/django/container-start.sh)
- currently there is a dummy mail service in place (registered with sendgrid by Steffen; needs to go to AWS SES)


# Things in .gitignore
This should an impression what still needs to be added to the public repo in order to work properly.

![image.png](/.attachments/image-4dfade01-5c15-4009-8663-104dd054f380.png)
-> the actual .gitignore is longer (incl unit tests). I just tried to screenshot the most interesting part.