```bash
scripts/setup.sh

docker-compose \
    -f docker-compose-test.yml \
    run --rm unit

docker build -t vfarcic/go-demo .

docker tag bilalislam/go-demo vfarcic/go-demo:1.0

docker tag bilalislam/go-demo vfarcic/go-demo:1.1

docker push bilalislam/go-demo

docker push bilalislam/go-demo:1.0

docker push bilalislam/go-demo:1.1

docker-compose up -d db app
```
