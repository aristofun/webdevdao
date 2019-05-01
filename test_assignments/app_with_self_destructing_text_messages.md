## Non-rails framework: text web-app with self-destructing messages

Build a web application, which creates text self-destructing
messages.

**Requirements**

A user opens the website and creates a message. The application generates a safe link to this saved message (such as: http://yourapp.com/message/ftr45e32fgv56d2 ).

The user should be able to choose a destruction option:

- destroy message after the first link visit

- destroy after 1 hour

All the messages stored on the server side should be encrypted using the AES algorithm (you can use any library for text encryption).

Cover your application with the unit and integration tests using
rspec.

**Technologies**

Use any non-rails framework (sinatra, hanami or any other) for ruby backend. Also please deploy your application to Heroku.

**Bonus points for implementing**

- message should be encrypted on the frontend side, using a password and should be sent to backend in an encrypted format (to view the message, the user should enter a correct password)

- self-destruction of messages after a given number of link visits or after a given number of hours