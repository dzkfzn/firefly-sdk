```
install java jdk
npm i @openapitools/openapi-generator-cli -g
openapi-generator-cli generate -i https://api-docs.firefly-iii.org/firefly-iii-6.2.21-v1.yaml -g typescript-fetch -o ./

npm version patch
npm version minor
npm version major

npm publish

npm run auto-run
```

