# scala-web-sbt-spring-jsp-challenge-question-bcrypt-encoded

## Description
A springboot challenge-question web app with jsp support.
Three roles are defined; USER, ADMIN, and SUPER. All roles
can access pages `/home`, `/login`, and `/about`. Only USER
can access `/user` and ADMIN only `/admin` whereas SUPER can
navigate to either and have its own `/super`. Each role
has an action USER=VIEW ONLY, ADMIN=READ/WRITE, SUPER=CREATE.
All password are encoded with bcrypt.

Presents a register form to create an inMemoryUser.
Once the user is created it is given the USER role
by default and auto logged in.

Presents a challenge-question form to challenge-question passwords on any user,
by default the user is reassigned USER role and auto
logged in. Only restriction on passwords are they match;
all validation is done client side.

Uses a challenge question on password rest and user register
to verify user. Customizes user data class by extending the
UserDetailService.

## Tech stack
- scala
- sbt
  - springboot
  - jsp
  - bootstrap
  - jquery
  - datatable

## Docker stack
- hseeberger/scala-sbt:11.0.2-oraclelinux7_1.3.5_2.12.10

## To run
`sudo ./install.sh -u`
Available at http://localhost
- Login with id: user and password: pass
- Login with id: admin and password: pass
- Login with id: super and password: pass

## To stop (optional)
`sudo ./install.sh -d`

## For help
`sudo ./install.sh -h`

## Credit
[Code concept](https://stackoverflow.com/questions/20227/how-do-i-use-3des-encryption-decryption-in-java)
