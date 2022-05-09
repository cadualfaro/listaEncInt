#include<stdio.h>
#include<stdlib.h>

class Nodo{
	public:
	int conteudo;
	Nodo * prox;
	
	Nodo(int val){
		conteudo = val;
		prox = NULL;
	}
};

class Lista{
	public:
	Nodo* prim;
	int tam;
	Lista(){
		prim = NULL;
	}
	
void inserir_inicio(int val){
	Nodo* novo = new Nodo(val);
	novo -> prox = prim;
	prim = novo;
}

void imprime(){
	
	Nodo* temp; //criaçãop de uma variável auxiliar para percorrer a lista
	for(temp = prim; temp != NULL; temp = temp->prox){
	printf("info = %d\n", temp->conteudo);
}
}

int somatorio(){//Somar valores da lista
	Nodo* sum;
	int total;
	for(sum = prim; sum != NULL; sum = sum->prox){
	total = sum->conteudo+total;
}
	printf("\nA soma dos valores da lista e: %d\n",total);
return total;
}

void imprime_positivos(){//imprime cada valor positivo presente na lista
	Nodo* pos;
	int pstv;
	for(pos = prim; pos != NULL; pos = pos->prox){
	pstv = pos-> conteudo;
	if(pstv>=0){
		printf("\nValor: %d\n",pstv);
	}
}
}

void Buscar(int valor){ 
	Nodo* k; //variável auxiliar para percorrer a lista
	int recebido;
	for(k = prim; k != NULL; k = k->prox){
		if(valor == k->conteudo){
			recebido = valor;
}
	}
	if(recebido == valor){
		printf("Encontrado!\n");
	}
			else{
			printf("Nao Encontrado!\n");
	}

}

void Exlcuir(Lista *lista, int valor){
	Nodo * noARemover = NULL;
	
	if(prim != NULL && lista-> prim-> conteudo == valor){
		noARemover = lista-> prim;
		lista-> prim = noARemover-> prox; 
		printf("Valor removido\n");
	}
	else{
		while(prim != NULL && prim-> prox != NULL && prim-> prox-> conteudo == valor){
		noARemover = prim-> prox;
		prim-> prox = noARemover-> prox;
		printf("Valor removido\n");
		}
		if(noARemover == NULL){
		printf("Valor nao encontrado\n");
		}
		
	}
	if(noARemover != NULL){
		free(noARemover);
	}
}

void Liberar(){
	Nodo* p;
	while(p != NULL){
		Nodo* t = p->prox;
		free(p);
		p = t;
	}
}
};


int main(){
	
	int menu;
	int valor;
	int num=0;
	
Lista * l; //declara uma lista não inicializada

l = new Lista(); // inicializa lista como vazia (limpa possível conteúdo da lista)

printf("Lista inicializada.\n");

do{
        printf("\nSelecione a opera%c%co que deseja realizar.\n",135,131/*Tabela ASCII*/);
            printf("1. Inserir\n");
                printf("2. Mostrar valores da lista\n");
                	printf("3. Buscar valor na lista\n");
                    	printf("4. Somatorio\n");
                        	printf("5. Imprimir valores positivos da lista\n");
                        		printf("6. Remover valor da lista\n");
                           			printf("7. Sair\n");
            
            scanf("%d",&menu);
            switch(menu){
            	
            case 1:
            	printf("Digite o valor a ser inserido: ");
            	scanf("%d",&valor);
            	l -> inserir_inicio(valor); //insere na lista o elemento digitado
            	printf("%d foi inserido na lista\n",valor);
            	break;
            	
            case 2:
            	l-> imprime();
            	break;
            
			case 3:
        		printf("Digite o numero que esta procurando: ");
        		scanf("%d", &num);
        		l-> Buscar(num);
        		break;
        		
			case 4:
        		l -> somatorio();
        		break;
        	
        	case 5:
        		l -> imprime_positivos();
        		break;
        		
    		case 6:
    			printf("Digite o numero que quer remover: ");
        		scanf("%d", &num);
    			l->Exlcuir(l, num);
    			break;
        	
			case 7:
        		break;
        	}
        	}while(menu != 7);
			l->Liberar();
	
	return 0;
}
