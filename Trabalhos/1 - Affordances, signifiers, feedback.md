# Análise: Componente de Controlo de Volume (Xiaomi HyperOS/MIUI)

Neste trabalho decidi fazer a análise do componente de controlo de volume, na interface de um smartphone Xiaomi (usando o meu como exemplo), como demonstrado nas imagens abaixo:

<div align="center">
  
### Estados do Componente

| Máximo | Meio | Baixo | Sem Som (Mudo) |
| :---: | :---: | :---: | :---: |
| <img width="100" alt="Volume Máximo" src="https://github.com/user-attachments/assets/4d8a25c1-aa76-4532-8e7c-ec5287ea4cd3" /> | <img width="100" alt="Volume a Meio" src="https://github.com/user-attachments/assets/51cc4de7-bc19-4243-ac31-430f01a0005f" /> | <img width="100" alt="Volume Baixo" src="https://github.com/user-attachments/assets/74513e2b-bdb8-474f-878c-f9b5182b364a" /> | <img width="100" alt="Sem Som" src="https://github.com/user-attachments/assets/c17defdd-b393-4d05-b420-de578aeaf24c" /> |

</div>

<br>

## Questões da Interface

**Que ações é que o elemento permite de facto?**

Permite ajustar o nível de volume de áudio do dispositivo (media, toques, alarmes, etc.), definindo a intensidade do som emitido pelo sistema.

---

**Que ações parece permitir (affordances)?**

A forma vertical em "pílula" ou barra deslizante cria a *affordance* exclusiva de agarrar e arrastar, sugerindo que o utilizador deve deslizar o dedo para cima e para baixo para ajustar o nível. O ícone do altifalante na base, por estar isolado, pode sugerir a *affordance* visual de um botão para silenciar, embora na prática não tenha essa funcionalidade.

---

**Que signifiers existem?**

- **Preenchimento de Cor:** A proporção da barra preenchida a branco em contraste com o fundo translúcido escuro é o principal *signifier* do nível atual de volume.
- **Ícone Dinâmico:** O ícone do altifalante adapta-se ao estado do volume. No máximo, exibe três ondas sonoras; a meio, reduz o número de ondas; num nível baixo, exibe apenas uma onda; e quando está totalmente sem som (mudo), o ícone muda para um altifalante com um traço diagonal.
- **Posição Inicial:** O facto de a barra preencher de baixo para cima sinaliza claramente que a base é o volume mínimo e o topo é o máximo.

---

**Algum signifier contraria a forma?**

Sim. O ícone do altifalante na base destaca-se como se fosse um botão individual e clicável para fazer "Mute" (silenciar rapidamente), mas clicar nele não executa qualquer ação, frustrando a expectativa visual. 
Por outro lado, em relação à barra em si, a forma não contraria a função: a aparência sugere que a interação tem de ser feita através do ato contínuo de arrastar o dedo, e na prática é exatamente essa a única forma de operar no ecrã tátil, uma vez que dar um toque (tap) noutro ponto da barra não faz o volume saltar para lá.

---

**Que feedback devolve, e quando?**

O feedback é exclusivamente visual e imediato. À medida que o utilizador arrasta o dedo na barra ou usa os botões físicos, a área branca da barra aumenta ou diminui instantaneamente acompanhando o movimento. Adicionalmente, o ícone do altifalante atualiza-se em tempo real para refletir o nível. O sistema não devolve qualquer feedback auditivo (como um "beep" de teste como se vê em dispositivos como computadores) nem feedback háptico (vibração) durante este ajuste.

---

**O que acontece quando existe alguma falha?**

Se ocorrer uma falha de software (ex: bloqueio do sistema de áudio), a barra de volume pode aparecer e mover-se visualmente no ecrã ao pressionar os botões, mas não haverá qualquer alteração real no som emitido pelas aplicações.

---

**Funciona sem visão ou sem rato?**

Sim. Tratando-se de um smartphone, a interação principal não usa rato, mas sim toque direto ou os botões físicos.

- **Sem visão (Acessibilidade/TalkBack):** O leitor de ecrã (TalkBack) foca no controlo de volume e anuncia o seu estado (ex: "Volume de multimédia, 50%, controlo de deslize"). O utilizador pode usar gestos específicos do TalkBack (como deslizar para cima ou para baixo com um dedo após selecionar a barra) ou os botões físicos para ajustar, recebendo confirmação vocal do novo nível.
- **Interação Alternativa (Botões Físicos):** O utilizador pode ajustar o volume sem interagir com o ecrã tátil, utilizando os botões físicos de volume (aumentar/diminuir) localizados na lateral do dispositivo. Esta é, de facto, a forma primária e mais comum de interagir com este componente, funcionando perfeitamente sem necessidade de olhar para o ecrã.
