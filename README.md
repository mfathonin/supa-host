# Supabase Docker

This setup for deploying supabase securely. All step explained in this [tutorial](https://youtu.be/wyUr_U6Cma4?si=7dU-564umAU5aUn2)

# Prepare to deploy

- Copy the `.env.example` to `.evn`
- Setup MinIO by running `docker-compose.s3.yml`. This will setup initial bucket that listed on MinIO configuration in `.env`

  ```bash
  docker compose -f docker-compose.s3.yml up -d
  ```

- Open MinIO console at http://localhost:9090 if you need to adjust/configure something
- Kill and remove the MinIO container

  ```bash
  docker compose -f docker-compose.s3.yml down -v --remove-orphans
  ```

# Deploy

- Just run the `docker-compose.yml` to deploy the Supabase

  ```bash
  docker compose -f docker-compose.yml up -d
  ```

---

> ##### _⚠️ Don't forget to manage your `.env` file before deploy to production. ⚠️_
