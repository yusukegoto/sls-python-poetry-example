Example app for https://github.com/serverless/serverless-python-requirements/issues/832

requirements:
  docker

How to reproduce
1. `npm install`
2. `npm run sls -- package --stage dev --verbose`

```
Error:
Running "docker run --rm -v /Users/yusukegoto/Library/Caches/serverless-python-requirements/ce48a8a22435647796953ce76e58d48e56f8188581b3394df24ca7e7f8340481_x86_64_slspyc:/var/task:z -v /Users/yusukegoto/Library/Caches/serverless-python-requirements/downloadCacheslspyc:/var/useDownloadCache:z -u 0 public.ecr.aws/sam/build-nodejs18.x:latest-x86_64 python -m pip install -t /var/task/ -r /var/task/requirements.txt --cache-dir /var/useDownloadCache" failed with: "WARNING: The requested image's platform (linux/amd64) does not match the detected host platform (linux/arm64/v8) and no specific platform was requested
/usr/bin/python: No module named pip"
```
