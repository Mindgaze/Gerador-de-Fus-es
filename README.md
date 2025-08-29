# Gerador-de-Fus-es
## Objetivo: Esse projeto se propõem a ser uma experiencia de VIbecoding com obejtivo de Fazer um gerador de imagem capaz de fundir duas imagens.

## Procedimento 
## Dia 0
Foi realizada uma ação de prompt enginering, baseada em zero shot prompting direcionadas ao influir que formato do output seja 9:16,  solicitado ao gemini v2.05 Pro o codigo para a versão 0 do projeto. Segue o prompt ultlizado:
"Create an python codd deployable on google colab to Make a ai image art generator it has to be able to fuse to i ages acording to the prompt. generate image size 9:16,Full Length Body Size View,the actual generated image resolution from the AI model 9:16 aspect ratio,The generate image must be generate in 9:16."

## Dia 1
O codigo gerado foi textado em ambiente colab. O codigo apresentou erro na etapa de importação do modelo. Minha hipotese é que O erro apresentado foi decorente das seguintes linhas, uma vez que que o ambiente Colab na forma que posso ultlizar não suporta tal recurso.  
"# Move the model to the GPU for faster processing
---> 17 pipe = pipe.to("cuda")"
 Elimianr as linhas  teve resultados positivos. O passo de importação do modelo e upload da primeira imagem teve sucesso. Entretanto um novo problema aparaceu na celula de geração da imagem em si. Entertanto a renderização da da imagem ainda estava viculado ao GPU ("cuda") levando a problemas. Optou-se por excluir menções a "cuda" e deixar o sistema alocar o melhor hardware disponivel
