release: python manage.py migrate
web: gunicorn config.wsgi:application
worker_and_beat: REMAP_SIGTERM=SIGQUIT celery -A config.celery_app worker -B --loglevel=info
