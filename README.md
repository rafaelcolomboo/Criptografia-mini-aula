# Criptografia-mini-aula
🔐 Projeto: Criptografia RSA em Rust
🧠 Introdução

A criptografia RSA é um dos métodos mais utilizados no mundo para proteger informações digitais. Criada em 1977 por Rivest, Shamir e Adleman, ela é um tipo de criptografia assimétrica, o que significa que usa duas chaves diferentes: uma pública e uma privada.

A ideia principal é simples: a chave pública é usada para criptografar mensagens, enquanto a chave privada é usada para descriptografar. Assim, mesmo que alguém intercepte os dados, não consegue entender o conteúdo sem possuir a chave correta.

⚙️ Funcionamento do RSA

O algoritmo RSA é baseado em conceitos matemáticos, especialmente em números primos e aritmética modular.

Primeiro, escolhem-se dois números primos grandes, chamados p e q. A multiplicação deles gera o valor n, que faz parte da chave pública e privada. Depois, calcula-se a função totiente de Euler, φ(n), que representa a quantidade de números menores que n que são coprimos com ele.

Em seguida, é escolhido um número e que seja coprimo com φ(n). Por fim, calcula-se o inverso modular de e, chamado d. Com esses valores, formam-se as chaves:

Chave pública: (n, e)

Chave privada: (n, d)

O processo de criptografia funciona elevando a mensagem (convertida em número) à potência de e, e depois aplicando o módulo n:

c = m^e mod n

Para descriptografar, faz-se o processo inverso usando a chave privada:

m = c^d mod n

Graças às propriedades matemáticas do RSA, o resultado final da descriptografia é exatamente a mensagem original.

🔒 Segurança e Aplicações

A segurança do RSA vem do fato de que fatorar números muito grandes é uma tarefa extremamente difícil e demorada. Quando n é formado por dois primos grandes, descobrir quais são esses primos é praticamente impossível com os computadores atuais.

Por isso, o RSA é amplamente usado em diferentes áreas, como:

Conexões seguras na web (HTTPS);

Assinaturas digitais e certificados;

Troca de chaves em protocolos como SSH.

⚡ Limitações

Mesmo sendo um algoritmo muito importante, o RSA tem algumas limitações. Ele é mais lento que outros tipos de criptografia, como o AES, e não é indicado para criptografar grandes volumes de dados.

Além disso, existe o risco futuro de que o RSA possa ser quebrado por computadores quânticos, que têm capacidade de fatorar números grandes muito mais rápido do que as máquinas atuais.

Por isso, o RSA costuma ser usado em conjunto com outros algoritmos — por exemplo, para proteger apenas a troca de chaves, enquanto outro método mais rápido cuida da criptografia dos dados em si.

🧩 Conclusão

O RSA é um exemplo clássico de como a matemática pode ser aplicada para garantir a segurança digital. Ele mostra que, com o uso inteligente de números primos e operações modulares, é possível proteger comunicações e informações de forma confiável.

Neste projeto, o objetivo foi implementar o RSA em Rust de forma educativa, entendendo na prática como gerar as chaves, criptografar e descriptografar mensagens, e visualizar como a teoria matemática se transforma em código.
