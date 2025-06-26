#docker run -d --name=roach1 --hostname=roach1 --net=roachnet -p 26257:26257 -p 8080:8080 -v "/home/ameya/Apps/cockroachDB/cockroach-data/roach1:/cockroach/cockroach-data" cockroachdb/cockroach start --insecure --join=roach1,roach2,roach3
#docker run -d --name=roach2 --hostname=roach2 --net=roachnet -v "/home/ameya/Apps/cockroachDB/cockroach-data/roach2:/cockroach/cockroach-data" cockroachdb/cockroach start --insecure --join=roach1,roach2,roach3
#docker run -d --name=roach3 --hostname=roach3 --net=roachnet -v "/home/ameya/Apps/cockroachDB/cockroach-data/roach3:/cockroach/cockroach-data" cockroachdb/cockroach start --insecure --join=roach1,roach2,roach3
#docker exec -it roach1 ./cockroach init --insecure

docker start roach1
docker start roach2
docker start roach3