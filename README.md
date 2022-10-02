README.md



# run STUN server 

export MIN_PORT=50000
export MAX_PORT=50010
docker run \
  -d \
  -p 3478:3478 \
  -p 3478:3478/udp \
  -p ${MIN_PORT}-${MAX_PORT}:${MIN_PORT}-${MAX_PORT}/udp \
  -e USERNAME=another_user \
  -e PASSWORD=another_password \
  -e REALM=another_realm \
  -e MIN_PORT=${MIN_PORT} \
  -e MAX_PORT=${MAX_PORT} \
  --restart=always \
  --name coturn \
  zenosmosis/docker-coturn
# you-through-me-native
