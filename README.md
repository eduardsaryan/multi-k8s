# Travis CI google key encryption

docker run -it -v $(pwd):/app ruby sh
gem install travis

travis login --github-token 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 --com
travis encrypt-file service-account.json -r  acronymattest/multi-k8s  --com

# Create secret for postgres
kubectl create secret generic pgpassword --from-literal PGPASSWORD=password