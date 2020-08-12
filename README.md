## Running the code

### Vue

Navigate to the `awesomechat-frontend directory`:

```bash
cd awesomechat-frontend
```

Install the dependencies from npm:

``` bash
npm install
```

Run the webpack dev server (starts on localhost:8080):

```bash
npm run dev
```

### Django

To get the Django server running:

Install the requirements from pip

```bash
pip install -r requirements.txt
```

Run django's development server (starts on localhost:8000):

```bash
python manage.py runserver
```

### RabbitMQ

awesomechat uses RabbitMQ to bridge the django application and the uWSGI WebSocket server. The installation process varies. Check the [docs](https://www.rabbitmq.com/download.html) on how you can install it for your platform.

### WebSocket server

awesomechat uses `uWSGI` as it's websocket server, if you've already installed the requirements from `requirements.txt` if should already be installed.

You can start it with

```bash
uwsgi --http :8081 --gevent 100 --module websocket --gevent-monkey-patch --master