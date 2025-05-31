sudo docker compose -f pwd.yml up
wait create site ..
go to frontend
sudo docker compose exec -it frontend bash
cd apps
bench get-app hrms
cd ../sites/frontend/
bench --site frontend list-apps
bench --site frontend install-app hrms
bench migrate --skip-failing
sudo docker compose exec -it backend bash
bench get-app hrms
bench --site frontend install-app hrms
bench migrate --skip-failing

