## Anotações de estudo

Arquivo provider.tf:
- Nele dá pra configurar qual **profile** de credencial o Terraform vai utilizar
- Por exemplo, no ~/.aws/credentials, pode ter dois profiles: o **default** e um de **lab**, cada um com diferentes Access Key e Access Secret

Trabalhando no laboratório do AWS Academy:
- o usuário criado para nós possui seu próprio Access Key. O "terraform" deve assumir a Role **LabRole** ao executar

**variables.tf** define o que o Terraform espera receber de variável no INPUT, pode ter valores variáveis

**variables.tfvars** normalmente não é versionado e possui os valores não-default das variáveis. Podemos ter .tfvars de diferentes environments (como dev e prod) com o mesmo código terraform

**outputs.tf** traz variáveis que são definidos após a execução, no OUTPUT, como ID de instância EC2, endereço IP público que a AWS alocou em tempo de execução