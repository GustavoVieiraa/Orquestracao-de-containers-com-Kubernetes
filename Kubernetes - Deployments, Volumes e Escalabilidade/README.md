<div align="center">
  <table>
    <tr>
      <td align="center">
        <!-- Link para o Certificado -->
        <a href="https://cursos.alura.com.br/certificate/gustavo-vieira17/kubernetes-deployments-volumes-escalabilidade">
          <img loading="lazy" width="128px" src="https://www.alura.com.br/assets/api/cursos/kubernetes-deployments-volumes-escalabilidade.svg" />
        </a>
        <h4>Curso</h4>
      </td>
      <td align="center">
        <!-- Link para o Certificado -->
        <a href="https://cursos.alura.com.br/certificate/gustavo-vieira17/kubernetes-deployments-volumes-escalabilidade">
          <img loading="lazy" width="128px" src="https://static.vecteezy.com/system/resources/previews/028/293/920/original/trophy-icon-3d-rendering-illustration-png.png" />
        </a>
        <h4>Certificado</h4>
      </td>
    </tr>
  </table>
  <h1>Kubernetes: Deployments, Volumes e Escalabilidade ☸️</h1>
</div>
<p align="right">
  <img loading="lazy" src="https://img.shields.io/badge/CARGA_HORARIA-8_HORAS_+_PRÁTICAS-yellow?style=for-the-badge"/>
  <img loading="lazy" src="http://img.shields.io/static/v1?label=STATUS&message=FINALIZADO!&color=GREEN&style=for-the-badge"/>
</p>

<div>
  <h2>Nesse curso, aprimorei minhas habilidades em orquestração de containers com Kubernetes, aprendendo a:</h2>
  <ul>
    <li><h3>Utilizar ReplicaSets e Deployments para garantir alta disponibilidade e facilitar atualizações de aplicações.</h3></li>
    <li><h3>Implementar Liveness Probes e Readiness Probes para monitoramento da saúde dos containers e gerenciamento inteligente de tráfego.</h3></li>
    <li><h3>Configurar Horizontal Pod Autoscaler (HPA) para escalar aplicações automaticamente baseado no uso de CPU.</h3></li>
    <li><h3>Persistir dados utilizando Volumes, PersistentVolumes e PersistentVolumeClaims para manter dados seguros e disponíveis.</h3></li>
    <li><h3>Trabalhar com Storage Classes para provisionamento dinâmico de armazenamento em ambientes cloud e locais.</h3></li>
    <li><h3>Implementar StatefulSets para gerenciar aplicações stateful que requerem identidade e armazenamento persistente estável.</h3></li>
  </ul>

  <h2>Tópicos abordados:</h2>
  <ul>
    <li><h3>ReplicaSets e Deployments</h3></li>
    <li><h3>Estratégias de Atualização (Rolling Update, Recreate)</h3></li>
    <li><h3>Liveness Probes e Readiness Probes</h3></li>
    <li><h3>Horizontal Pod Autoscaler (HPA)</h3></li>
    <li><h3>Metrics Server</h3></li>
    <li><h3>Volumes e Tipos de Volumes (emptyDir, hostPath, PersistentVolume)</h3></li>
    <li><h3>PersistentVolumes (PV) e PersistentVolumeClaims (PVC)</h3></li>
    <li><h3>Storage Classes</h3></li>
    <li><h3>StatefulSets</h3></li>
    <li><h3>Provisionamento Dinâmico de Armazenamento</h3></li>
  </ul>
</div>
<br>
<div align="center">
  <h1> 🚀 Projeto Prático: Portal de Notícias com Alta Disponibilidade </h1>
  <p>Durante o curso, evolui o sistema de portal de notícias utilizando recursos avançados do Kubernetes, aplicando conceitos de:</p>
  <ul align="left">
    <li><b>Deployments:</b> Migração de Pods simples para Deployments com múltiplas réplicas e controle de versão</li>
    <li><b>Health Checks:</b> Implementação de Liveness e Readiness Probes para garantir disponibilidade e estabilidade</li>
    <li><b>Autoscaling:</b> Configuração de HPA com Metrics Server para escalamento automático baseado em CPU</li>
    <li><b>Persistência:</b> Configuração de volumes para persistir dados do banco de dados MySQL</li>
    <li><b>Storage Classes:</b> Utilização de provisionamento dinâmico para gerenciamento eficiente de armazenamento</li>
    <li><b>StatefulSets:</b> Implementação para aplicações stateful com identidade de rede e armazenamento estável</li>
  </ul>
  <br>
  <h2>📋 Estrutura de Arquivos YAML</h2>
  <p>O projeto inclui arquivos de definição para:</p>
  <ul align="left">
    <li>Deployments: <code>portal-noticias-deployment.yaml</code>, <code>sistema-noticias-deployment.yaml</code>, <code>db-noticias-deployment.yaml</code></li>
    <li>ReplicaSets: <code>portal-noticias-replicaset.yaml</code></li>
    <li>HPA: <code>portal-noticias-hpa.yaml</code></li>
    <li>Volumes: <code>pod-volume.yaml</code></li>
    <li>Metrics Server: <code>components.yaml</code></li>
  </ul>
</div>
