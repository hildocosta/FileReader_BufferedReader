<p align="center">
  <img src="https://github.com/hildocosta/hildocosta-Curso-Java--Nelio-Alves/blob/main/logo.png" width="300">
</p>

<h1 align="center">🚀 Explorando Leitura de Arquivo Texto em Java</h1>

<p>🔥 Bem-vindo ao repositório dedicado à exploração da leitura de arquivos de texto na linguagem de programação Java. Aqui, você encontrará informações e exemplos práticos sobre como usar as classes FileReader e BufferedReader para ler e processar dados de arquivos de texto em seus programas Java.</p>

<p>🎓 Este repositório é voltado para estudantes e desenvolvedores que desejam aprender como ler dados de arquivos de texto de forma eficiente e prática em Java. Aqui, você encontrará explicações detalhadas, exemplos de código e exercícios para aprimorar suas habilidades de leitura de arquivos.</p>

<p>💡 Ao explorar a leitura de arquivos texto em Java, você aprenderá como abrir, ler e processar dados de arquivos de texto usando as classes FileReader e BufferedReader. Essas classes fornecem métodos simples e eficazes para trabalhar com arquivos de texto, permitindo que você extraia informações de arquivos de forma fácil e rápida.</p>

<h2 align="center">🔒 Licença</h2>

<p>⚖️ Este projeto está licenciado sob a <a href="LICENSE">Licença MIT</a>.</p>

<h2 align="center">📧 Contato</h2>

<h3>🔗 Redes Sociais e Contato</h3>

<ul>
  <li>📌 GitHub: <a href="https://github.com/hildocosta">hildocosta</a></li>
  <li>💼 LinkedIn: <a href="https://www.linkedin.com/in/hildo-costa-b83812231/">Hildo Costa</a></li>
  <li>✉️ Email: hildo.costa@pm.pr.gov.br</li>
</ul>

<p>Agora que estamos preparados, vamos explorar como ler arquivos de texto em Java!</p>

<h2 align="center">🚀 Vamos Começar</h2>

<h3>🔥 Leitura de Arquivo Texto em Java</h3>

<p>Para ler dados de um arquivo de texto em Java, você pode usar as classes FileReader e BufferedReader. A classe FileReader é usada para ler caracteres de um arquivo, enquanto a classe BufferedReader é usada para ler texto de uma entrada de caractere.</p>

<p>Veja um exemplo de código para ler um arquivo de texto em Java usando FileReader e BufferedReader:</p>

```java
import java.io.BufferedReader;
import java.io.FileReader;
import java.io.IOException;

public class Main {

    public static void main(String[] args) {
        
        String caminho = "caminho/do/arquivo.txt";
        
        try (BufferedReader br = new BufferedReader(new FileReader(caminho))) {
            String linha = br.readLine();
            while (linha != null) {
                System.out.println(linha);
                linha = br.readLine();
            }
        } catch(IOException e) {
            System.out.println("Erro ao ler o arquivo: " + e.getMessage());
        }
    }
}
