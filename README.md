# Docker Compose Radicale

## Usage
Rename the `.env.example` file into `.env`.

Set the `LISTEN_ADDRESS` to the address you want radicale to be available on. Note that this address should be assigned to an interface on the host running docker.

Change the cpu and memory limits if you are planning to support more than a few users.

Rename the `users.example` file into `users`

Add colon separated `<username>:<password>` pairs

Run `docker compose up`

The server should be accessible on `http://<LISTEN_ADDR>:5232`.

## Security
This server does *NOT* encrypt user passwords. This is a deliberate decision as I am running on a trusted machine behind a VPN. If you want to use this in a less scuffed way or you want to make this server accessible from the internet, the [Radicale documentation](https://radicale.org/v3.html#the-secure-way) has you covered.