# Comandos Básicos do Vagrant

O Vagrant é uma ferramenta popular para gerenciar ambientes de desenvolvimento virtualizados, e o VirtualBox é uma das opções comuns para a virtualização. Aqui está uma lista de comandos essenciais e técnicas para trabalhar com Vagrant e VirtualBox:

**Comandos Básicos do Vagrant:**

1. **`vagrant init`:** Cria um novo Vagrantfile (arquivo de configuração do Vagrant) em um diretório.

2. **`vagrant up`:** Inicializa e provisiona (se necessário) uma máquina virtual de acordo com as configurações definidas no Vagrantfile.

3. **`vagrant ssh`:** Conecta-se à máquina virtual via SSH.

4. **`vagrant halt`:** Desliga a máquina virtual de forma segura.

5. **`vagrant destroy`:** Remove completamente a máquina virtual.

6. **`vagrant suspend`:** Pausa o estado atual da máquina virtual.

7. **`vagrant resume`:** Retoma uma máquina virtual pausada.

**Configuração do Vagrantfile:**

8. **Configuração da Box:** Especifique uma imagem de máquina virtual (box) no Vagrantfile. Por exemplo:

   ```ruby
   config.vm.box = "ubuntu/bionic64"
   ```

9. **Configuração de Rede:** Defina configurações de rede, como encaminhamento de portas e configuração de adaptadores de rede.

   ```ruby
   config.vm.network "forwarded_port", guest: 80, host: 8080
   ```

10. **Provisionamento:** Especifique scripts ou comandos de provisionamento para configurar a máquina virtual.

   ```ruby
   config.vm.provision "shell", path: "bootstrap.sh"
   ```

**Comandos Avançados:**

11. **`vagrant reload`:** Reinicializa a máquina virtual, aplicando alterações no Vagrantfile.

12. **`vagrant provision`:** Execute o provisionamento manualmente sem reiniciar a máquina virtual.

**Plugins do Vagrant:**

13. **Instalação de Plugins:** O Vagrant possui uma extensa coleção de plugins que adicionam funcionalidades adicionais. Você pode instalá-los usando o comando `vagrant plugin install`.

**Integração com o VirtualBox:**

14. **`vagrant up --provider virtualbox`:** Use este comando para especificar o provedor (no caso, VirtualBox) ao iniciar uma máquina virtual. Isso é útil se você tiver múltiplos provedores instalados.

15. **Configurações do VirtualBox:** Você pode configurar opções específicas do VirtualBox diretamente no Vagrantfile, como memória, CPUs, nome da máquina, etc.

**Gerenciamento de Boxes:**

16. **`vagrant box list`:** Liste todas as boxes disponíveis no sistema.

17. **`vagrant box add`:** Adicione uma nova box ao sistema.

18. **`vagrant box remove`:** Remova uma box existente do sistema.

Esses são alguns dos comandos e técnicas essenciais para trabalhar com o Vagrant e o VirtualBox. Lembre-se de que a configuração específica pode variar dependendo do seu caso de uso e das necessidades do projeto. Certifique-se de consultar a documentação oficial do Vagrant e do VirtualBox para obter informações detalhadas e exemplos adicionais.

___________________
## Oficina de Linux
