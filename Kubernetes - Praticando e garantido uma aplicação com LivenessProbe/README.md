<div align="center">
  <table>
    <tr>
      <td align="center">
        <!-- Link para o Certificado -->
        <a href="https://cursos.alura.com.br/user/gustavo-vieira17/course/kubernetes-praticando-garantido-aplicacao-livenessprobe/certificate">
          <img loading="lazy" width="128px" src="https://www.alura.com.br/assets/api/cursos/kubernetes-praticando-garantido-aplicacao-livenessprobe.svg" />
        </a>
        <h4>Curso</h4>
      </td>
      <td align="center">
        <!-- Link para o Certificado -->
        <a href="https://cursos.alura.com.br/user/gustavo-vieira17/course/kubernetes-praticando-garantido-aplicacao-livenessprobe/certificate">
          <img loading="lazy" width="128px" src="https://static.vecteezy.com/system/resources/previews/028/293/920/original/trophy-icon-3d-rendering-illustration-png.png" />
        </a>
        <h4>Certificado</h4>
      </td>
    </tr>
  </table>
  <h1>Kubernetes: Praticando e Garantindo uma Aplicação com LivenessProbe ☸️</h1>
</div>
<p align="right">
  <img loading="lazy" src="https://img.shields.io/badge/CARGA_HORARIA-8_HORAS_+_PRÁTICAS-yellow?style=for-the-badge"/>
  <img loading="lazy" src="http://img.shields.io/static/v1?label=STATUS&message=FINALIZADO!&color=GREEN&style=for-the-badge"/>
</p>

<div>
  <h2>Nesse curso, consolidei meus conhecimentos em Kubernetes através de um projeto prático completo, aprendendo a:</h2>
  <ul>
    <li><h3>Implementar uma aplicação real (Voll.med API) no Kubernetes utilizando Deployments e múltiplas réplicas para alta disponibilidade.</h3></li>
    <li><h3>Configurar banco de dados MySQL com StatefulSets garantindo persistência de dados e identidade estável.</h3></li>
    <li><h3>Utilizar PersistentVolumes e PersistentVolumeClaims para armazenamento persistente com provisionamento dinâmico via Storage Classes.</h3></li>
    <li><h3>Implementar Liveness Probes para monitoramento automático da saúde da aplicação e recuperação de falhas.</h3></li>
    <li><h3>Gerenciar configurações sensíveis utilizando Secrets com criptografia Base64 para proteção de credenciais.</h3></li>
    <li><h3>Configurar Services do tipo LoadBalancer para exposição segura e eficiente da aplicação em produção.</h3></li>
    <li><h3>Utilizar ConfigMaps para desacoplar variáveis de ambiente e facilitar a gestão de configurações.</h3></li>
    <li><h3>Implementar backups automatizados utilizando CronJobs para garantir a segurança dos dados.</h3></li>
  </ul>

  <h2>Tópicos abordados:</h2>
  <ul>
    <li><h3>Deployments e Estratégias de Deploy</h3></li>
    <li><h3>StatefulSets para Aplicações Stateful</h3></li>
    <li><h3>Liveness Probes e Health Checks</h3></li>
    <li><h3>PersistentVolumes (PV) e PersistentVolumeClaims (PVC)</h3></li>
    <li><h3>Storage Classes e Provisionamento Dinâmico</h3></li>
    <li><h3>Secrets e Segurança de Credenciais</h3></li>
    <li><h3>ConfigMaps para Gerenciamento de Configurações</h3></li>
    <li><h3>Services (ClusterIP, NodePort, LoadBalancer)</h3></li>
    <li><h3>CronJobs para Tarefas Agendadas</h3></li>
    <li><h3>Volumes Persistentes e Montagem de Discos</h3></li>
    <li><h3>Container Storage Interface (CSI)</h3></li>
  </ul>
</div>
<br>
<div align="center">
  <h1> 🚀 Projeto Prático: Sistema Voll.med - API de Gerenciamento Médico </h1>
  <p>Durante o curso, desenvolvi e implantei uma aplicação completa de gerenciamento médico (Voll.med API) utilizando todos os recursos avançados do Kubernetes:</p>
  
  <h2>🏗️ Arquitetura da Aplicação</h2>
  <ul align="left">
    <li><b>Deployment da API:</b> 3 réplicas da aplicação Voll.med com Liveness Probes configurados na rota <code>/paciente</code></li>
    <li><b>StatefulSet MySQL:</b> Banco de dados MySQL 8 com persistência de dados e identidade estável</li>
    <li><b>PersistentVolume:</b> 8Gi de armazenamento persistente com Storage Class <code>csi-hostpath-sc</code></li>
    <li><b>LoadBalancer Service:</b> Exposição da API na porta 3000 com balanceamento de carga automático</li>
    <li><b>ClusterIP Service:</b> Serviço interno para comunicação com o banco de dados MySQL</li>
    <li><b>ConfigMaps:</b> Variáveis de ambiente para DB_DATABASE e DB_HOST</li>
    <li><b>Secrets:</b> Credenciais criptografadas para DB_USER e DB_PASSWORD</li>
    <li><b>CronJob:</b> Backup automático do banco de dados agendado para 03:00 diariamente</li>
  </ul>
  
  <br>
  <h2>🔧 Implementação Técnica</h2>
  
  <h3>1. Banco de Dados com StatefulSet</h3>
  <ul align="left">
    <li>Utilização de StatefulSet para garantir persistência e evitar inconsistência de dados</li>
    <li>Configuração de <code>terminationGracePeriodSeconds</code> para salvamento seguro de dados</li>
    <li>Volume persistente montado em <code>/var/lib/mysql</code></li>
    <li>Service headless (ClusterIP: None) para acesso estável ao banco</li>
  </ul>

  <h3>2. Armazenamento Persistente</h3>
  <ul align="left">
    <li>PersistentVolumeClaim com modo de acesso <code>ReadWriteOnce</code></li>
    <li>Storage Class <code>csi-hostpath-sc</code> para provisionamento dinâmico</li>
    <li>Driver CSI habilitado no Minikube para acesso ao armazenamento local do host</li>
    <li>Capacidade de 8Gi garantindo espaço adequado para o banco de dados</li>
  </ul>

  <h3>3. Deployment da Aplicação</h3>
  <ul align="left">
    <li>3 réplicas para alta disponibilidade e distribuição de carga</li>
    <li>Imagem customizada <code>gustavovieiradev/vollmed-api:1</code> publicada no Docker Hub</li>
    <li>Variáveis de ambiente injetadas via ConfigMaps e Secrets</li>
    <li>Liveness Probe com verificação HTTP a cada 3 segundos após 60 segundos de inicialização</li>
  </ul>

  <h3>4. Segurança e Configuração</h3>
  <ul align="left">
    <li><b>ConfigMaps:</b> Dados não sensíveis (DB_DATABASE: testemed, DB_HOST: mysql)</li>
    <li><b>Secrets:</b> Credenciais criptografadas em Base64 (DB_USER: root, DB_PASSWORD)</li>
    <li>Separação clara entre configurações públicas e dados confidenciais</li>
  </ul>

  <h3>5. Exposição e Acesso</h3>
  <ul align="left">
    <li>LoadBalancer Service para acesso externo na porta 3000</li>
    <li>Minikube tunnel para simular LoadBalancer em ambiente local</li>
    <li>Balanceamento automático de carga entre as 3 réplicas</li>
  </ul>

  <h3>6. Backup Automatizado</h3>
  <ul align="left">
    <li>CronJob agendado para executar diariamente às 03:00</li>
    <li>Utilização da imagem <code>leonardosartorello/mysqldump:v4</code></li>
    <li>Acesso às credenciais via ConfigMaps e Secrets</li>
  </ul>

  <br>
  <h2>📋 Estrutura de Arquivos YAML</h2>
  <p>O projeto inclui os seguintes arquivos de configuração:</p>
  <ul align="left">
    <li><code>app.yaml</code> - Deployment da aplicação Voll.med com 3 réplicas e Liveness Probe</li>
    <li><code>mysql.yaml</code> - StatefulSet do MySQL, Service, PVC e CronJob de backup</li>
    <li><code>services.yaml</code> - LoadBalancer Service para exposição da API</li>
    <li><code>configmaps.yaml</code> - ConfigMap com variáveis de ambiente do banco</li>
    <li><code>secrets.yaml</code> - Secret com credenciais criptografadas</li>
  </ul>

  <br>
  <h2>✅ Ambiente Configurado e Testado</h2>
  <p>O ambiente foi completamente configurado localmente utilizando Minikube e Docker Desktop, com todos os recursos funcionando corretamente:</p>
  
  <h3>Configuração do Cluster</h3>
  <img src="https://raw.githubusercontent.com/GustavoVieiraa/Orquestracao-de-containers-com-Kubernetes/refs/heads/main/Kubernetes%20-%20Praticando%20e%20garantido%20uma%20aplica%C3%A7%C3%A3o%20com%20LivenessProbe/ClusterConfigOK.png" alt="Cluster Kubernetes Configurado" />
  <p><i>Cluster Kubernetes totalmente configurado com todos os recursos (Deployments, StatefulSets, Services, PVCs) em execução</i></p>

  <br>
  <h3>Testes de Requisição</h3>
  <img src="https://raw.githubusercontent.com/GustavoVieiraa/Orquestracao-de-containers-com-Kubernetes/refs/heads/main/Kubernetes%20-%20Praticando%20e%20garantido%20uma%20aplica%C3%A7%C3%A3o%20com%20LivenessProbe/testeRequisicaoOK.png" alt="Testes de Requisição Bem-Sucedidos" />
  <p><i>API Voll.med respondendo corretamente às requisições através do LoadBalancer com balanceamento entre as réplicas</i></p>

  <br>
  <h2>🎯 Resultados Alcançados</h2>
  <ul align="left">
    <li>✅ Aplicação rodando com alta disponibilidade (3 réplicas)</li>
    <li>✅ Banco de dados persistente e estável com StatefulSet</li>
    <li>✅ Health checks automáticos garantindo disponibilidade contínua</li>
    <li>✅ Armazenamento persistente com provisionamento dinâmico</li>
    <li>✅ Segurança de credenciais com Secrets criptografados</li>
    <li>✅ Exposição segura via LoadBalancer</li>
    <li>✅ Backups automatizados do banco de dados</li>
    <li>✅ Ambiente local totalmente funcional e testado</li>
  </ul>
</div>
