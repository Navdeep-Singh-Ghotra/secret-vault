# secret-vault
Hashicorp vault

Install vault on linux
```
wget -O - https://apt.releases.hashicorp.com/gpg | sudo gpg --dearmor -o /usr/share/keyrings/hashicorp-archive-keyring.gpg
echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/hashicorp-archive-keyring.gpg] https://apt.releases.hashicorp.com $(lsb_release -cs) main" | sudo tee /etc/apt/sources.list.d/hashicorp.list
sudo apt update && sudo apt install vault
```

```
export VAULT_ADDR='http://127.0.0.1:8200'
export VAULT_TOKEN='<root-token>'
vault kv put secret/hello foo=world
vault kv get secret/hello
```


