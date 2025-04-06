# Docker
docker compose build
docker compose up -d

# Docker db
docker exec -it db psql -U postgres
docker exec -it db psql -U postgres 

# Docker backend
docker exec -it backend npx prisma migrate dev --name init
docker exec -it backend npx prisma generate
docker exec -it backend npx prisma db push
docker exec -it backend npx prisma db pull
docker exec -it backend npx prisma studio

docker compose start
docker compose stop
