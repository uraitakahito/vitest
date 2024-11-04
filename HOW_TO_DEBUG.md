Build your docker image and run the container:

```console
% cd ~/projects/vitest && PROJECT=$(basename `pwd`) && docker image build -t $PROJECT-image . --build-arg user_id=`id -u` --build-arg group_id=`id -g` && docker container run -d --rm --init -e NODE_ENV=test --mount type=bind,src=`pwd`,dst=/app --mount type=bind,src=$HOME/.gitconfig,dst=/home/developer/.gitconfig --name $PROJECT-container $PROJECT-image && bell
```

1. Click on the "Run and Debug" icon in the activity bar of the editor.

2. Click on the "Javascript Debug Terminal" button.

```console
% cd test/core
% pnpm run test run test/basic.test.ts
```
