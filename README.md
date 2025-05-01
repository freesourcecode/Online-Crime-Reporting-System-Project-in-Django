# Online Crime Reporting System Project in Django with Source Code

An **Online Crime Reporting System in Django** is an easy project for beginners to learn how to build a web-based **Python** **Django** project.

We will provide you with the complete source code and database for the python project so that you can easily install it on your machine and learn how to program in Python Django.

This project online reporting system for the crime related incidents that happened with you.

>[!NOTE]
> To start creating a Online Crime Reporting System Project in **Python Django**, makes sure that you have PyCharm Professional IDE Installed in your computer.

## User Features of Online Crime Reporting System in Django

* **Manage User Profile**

For the user profile, The user can update his/her information details.

* **Registration**

For the registration, The user need to register first to create their own account.

* **Add Complaint**

For the complaint, The user can view and add complaint through this website.

*  **Login**

By default the user need to login first to enable to access the system.

## How to Create a Project an Online Crime Reporting System in Django?
   
Here are the steps on **how to create an Online Crime Reporting System Project in Django.**

1. **Open file**.

First, open “pycharm professional” after that click “file” and click “new project”.

2. **Choose Django**.

Next, after click “new project“, choose “Django” and click.

3. **Select file location**.

Then, select a file location wherever you want.

4. **Create application name**.

After that, name your application.

5. **Click create**.

Lastly, finish creating project by clicking “create” button.

6. **Start Coding**.

Finally, we will now start adding functionality to our Django Framework by adding some functional codes.

## Functionality and Codes of the Online Crime Reporting System in Django

* **Create template for the login in form in Online Crime Reporting System Django**.

In this section, we will learn on how create a templates for the student form. 

To begin with, add the following code in your login.html under the folder of templates/accounts/.

```
{% extends 'base.html' %}

{% block header %}
    <title>User Login</title>
    {% load static %}
    <link rel="stylesheet" href="{% static 'css/register.css' %}">
{% endblock %}

{% block content %}
    {% load widget_tweaks %}
    {% if error_message %}
        <p>{{ error_message }}</p>
    {% endif %}

   <div class="w-50 mx-auto my-3">
   <h4 class="text-center mx-auto my-3">User Login</h4>
        <form method="post" action="{% url 'accounts:login' %}">
              {% csrf_token %}

              <div class="form-group">
                  <label for="username">Username:</label>
                  <input class="form-control" type="text" name="username" placeholder="Username">
              </div>

              <div class="form-group">
                  <label for="password">Password</label>
                  <input class="form-control" type="password" name="password" placeholder="Your Password">
              </div>

              <div class="container text-center">
                  <input type="submit" class="btn btn-danger col-md-4" name="" value="Login">
                  <button class="btn btn-success col-md-4"><a href="{% url 'accounts:register' %}" class="text-white">Register</a></button>
              </div>

        </form>
    </div>

{% endblock %}
```

* **Create template for the user registration**

In this section, we will learn on how create a templates for the user registration. 

To start with, add the following code in your register.html under the folder of templates/account.

```
{% extends 'base.html' %}
{% load static %}

{% block header %} <title>User Registration</title>
<link rel="stylesheet" href="{% static 'css/register.css' %}">
{% endblock %}



{% block content %}
    <div class="container w-50 mx-auto my-3">
        <h4 class="text-center">REGISTRATION FORM</h4>
        <form enctype="multipart/form-data" method="post">{% csrf_token %}
        {% load widget_tweaks %}

        {% if messages %}
            {% for message in messages %}
                <div class="alert-danger">{{ message }}</div>
            {% endfor %}
        {% endif %}

        <div class="form-group">
            <label for="{{ form.username_for_label }}">Choose Your Username:</label>
            {{ form.username|add_class:"form-control" }}
        </div>

        <div class="form-group">
            <label for="{{ form.first_name_for_label }}">Your First Name:</label>
            {{ form.first_name|add_class:"form-control" }}
        </div>

        <div class="form-group">
            <label for="{{ form.last_name_for_label }}">Your Last Name:</label>
            {{ form.last_name|add_class:"form-control" }}
        </div>

        <div class="form-group">
            <label for="{{ form.email_for_label }}">Your Email:</label>
            {{ form.email|add_class:"form-control" }}
        </div>

        <div class="form-group">
            <label for="{{ form.password1_for_label }}">Your Password:</label>
            {{ form.password1|add_class:"form-control" }}
        </div>

        <div class="form-group">
            <label for="{{ form.password2_for_label }}">Confirm Your Password:</label>
            {{ form.password2|add_class:"form-control" }}
        </div>

        <div class="form-group">
            <label for="{{ form.bio_for_label }}">Your Biography in Short:</label>
            {{ form.bio|add_class:"form-control" }}
        </div>

        <div class="form-group">
            <label for="{{ form.profile_image_for_label }}">Upload Your Profile Picture:</label>
            {{ form.profile_image|add_class:"form-file-control" }}
        </div>

        <div class="form-group">
            <label for="{{ form.phone_no_for_label }}">Your Phone Number:</label>
            {{ form.phone_no|add_class:"form-control" }}
        </div>

        <div class="container text-center w-50">
            <input type="submit" class="btn-lg btn-success" value="REGISTER">
        </div>

    </form>
</div>
{% endblock %}
```

### 📌Here's the full documentation for the [Online Crime Reporting System Project in Django](https://itsourcecode.com/free-projects/python-projects/online-crime-reporting-system-project-in-django-with-source-code/)



