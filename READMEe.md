# ttesting


mkdir -p ~/.ssh
ssh-keyscan -t rsa github.com >> ~/.ssh/known_hosts
echo "${{ secrets.MIRROR_TOKEN }}" > ~/.ssh/id_rsa
chmod 0400 ~/.ssh/id_rsa
ls -la ~/.ssh
eval $(ssh-agent -s)
ssh-add ~/.ssh/id_rsa