				V�RI�VEIS
public vector2; vetor com cordenadas x e y e aparece no inspector
public gameobject cubo;

public persof posicao;
public float receb;
receb = posicao.angulo; // n�o esquecer de confiigurar na unity

__________________________________________________________________________

			Fun��es
if(Input.getkeydow("tecla")){Faz alguma coisa } // Clicar na tela
		 // getkey acontece sempre // getkeyrun quando n�o clicar


body = GetComponent<Rigidbody2D>(); // a vari�vel body pega o rigbody para poder fazer modifica��es

https://docs.unity3d.com/ScriptReference/Transform-position.html
https://www.youtube.com/watch?v=xolkyYkczZI // queda livre
https://docs.unity3d.com/ScriptReference/KeyCode.html // teclas 
https://unity3d.com/pt/learn/tutorials/topics/scripting/getbutton-and-getkey // como coloca tecla
https://www.youtube.com/watch?v=AnY1zeiorwE // robozinho

__________________________________________________________________________
Atalhos
F --> foca no objeto
w --> dire��o
r --> tamanho
e --> angulo


--> corpo fizico 
public Rigidbody2D body; // rigidez do corpo
add componet >> phisic2d >> rigidbody2d --> massa, gravidade e etc

--> criando ch�o: cria um novo componente em branco >> insere um boxcolider2d
--> insere um box colider no personagem 

__________________________________________________________________________

void FixedUpdate() { // apenas um �nico frame
         float h = Input.GetAxis("Horizontal");
        //body.velocity = new Vector2(velo * h , body.velocity.y);
            if (h == 0) { j = 0; } else { j = 1; }
        body.AddForce(Vector2.up * j * velo);
        body.AddForce(Vector2.right * h * velo);
}