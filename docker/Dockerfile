From frappe/erpnext:v15.63.0

RUN bench get-app hrms
RUN bench --site frontend install-app hrms
RUN bench migrate --skip-failing

CMD ["/home/frappe/frappe-bench/env/bin/gunicorn" "--chdir=/home/frappe/frappe-bench/sites" "--bind=0.0.0.0:8000" "--threads=4" "--workers=2" "--worker-class=gthread" "--worker-tmp-dir=/dev/shm" "--timeout=120" "--preload" "frappe.app:application"]
