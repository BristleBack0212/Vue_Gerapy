# Gerapy

Distributed Crawler Management Framework Based on Scrapy, Scrapyd, Scrapyd-Client, Scrapyd-API, Django and Vue.js.

## Support

Gerapy is developed based on Python 3.x. Python 2.x may be supported later.

## Usage

Install Gerapy by pip:

```bash
pip3 install gerapy
```

After the installation, you need to do these things below to run Gerapy server:

If you have installed Gerapy successfully, you can use command `gerapy`. If not, check the installation.

First use this command to initialize the workspace:

```bash
gerapy init
```

Now you will get a folder named `gerapy`. Also you can specify the name of your workspace by this command:

```
gerapy init <workspace>
```

Then `cd` to this folder, and run this command to initialize the Database:

```bash
cd gerapy
gerapy migrate
```

Next you need to create a superuser by this command:

```
gerapy createsuperuser
```

Then you can runserver by this command:

```bash
gerapy runserver
```

Then you can visit [http://localhost:8000](http://localhost:8000) to enjoy it. Also you can vist [http://localhost:8000/admin](http://localhost:8000/admin) to get the admin management backend.

If you want to run Gerapy in public, just run like this:

```
gerapy runserver 0.0.0.0:8000
```

Then it will run with public host and port 8000.

In Gerapy, You can create a configurable project and then configure and generate code of Scrapy automatically. But this module is unstable, we're trying to refine it.

Also you can drag your Scrapy Project to `projects` folder. Then refresh web, it will appear in the Project Index Page and comes to un-configurable, but you can edit this project through the web page.

As for deployment, you can move to Deploy Page. Firstly you need to build your project and add client in the Client Index Page, then you can deploy the project just by clicking button.

After the deployment, you can manage the job in Monitor Page.

## Docker

Just run this command:

```
docker-compose up
```

Then it will run at port 8000. You can use the temp admin account (username: admin, password: admin) to login. And please change the password later for safety.

Command Usage:

```
docker run -d -v <workspace>:/home/gerapy -p <public_port>:<container_port> germey/gerapy
```

Please specify your workspace to mount Gerapy workspace by `-v <workspace>:/app/gerapy` and specify server port by `-p <public_port>:<container_port>`.

If you run Gerapy by Docker, you can visit Gerapy website such as [http://localhost:8000](http://localhost:8000) and enjoy it, no need to do other initialzation things.

## TodoList

- [x] Add Visual Configuration of Spider with Previewing Website
- [x] Add Scrapyd Auth Management
- [x] Add Gerapy Auth Management
- [x] Add Timed Task Scheduler
- [ ] Add Visual Configuration of Scrapy
- [ ] Add Intelligent Analysis of Web Page

