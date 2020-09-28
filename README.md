# piSenac_rpg_texto




import java.util.Random;
import java.util.Scanner;

public class novovo {
    
    static Scanner rpg = new Scanner (System.in);
    
    static String nome;
    
    //Strings e vars fase03PH
    static int inimigo = 70;
    static int vida = 100;
    static String inventario = "sabre de luz";
    static int escolha;
    static int dano;
    static String nomeAMG;
    String mapa = rpg.nextLine();
    static int ataque;
    static int Sabre = 15;
    
    //Strings fase03UE:
    static String acessorioPlayer01 = "Sabre de Luz";
    static String forca = "Força";
    static String soco = "Soco";
    static Scanner leitor = new Scanner(System.in);

    //Vida e dano fase03UE:
    static int vidaPadawan = 100;
    static int vidaTropas = 50;
    static int vidaSTE = 55;
    static int vidaDV = 100;
    static int poderSabre = 20;
    static int poderForca = 25;
    static int damageDV = 20;
  
    public static void main(String[] args) {
    fase01();}
    
    static void fase01() {
        int var = 0;
        System.out.println(" "
    + "     _                                      \n" +
"  ___| |_ __ _ _ __  __      ____ _ _ __ ___ \n" +
" / __| __/ _` | '__| \\ \\ /\\ / / _` | '__/ __|\n" +
" \\__ \\ || (_| | |     \\ V  V / (_| | |  \\__ \\\n" +
" |___/\\__\\__,_|_|      \\_/\\_/ \\__,_|_|  |___/");
        
        System.out.println("\n\nHá muito tempo, numa galáxia muito, muito distante...");
        System.out.println("Um(a) jovem Padawan treinado por Luke Skywalker, está  ");
        System.out.println("a procura de seu mestre, com apenas alguns flashes de memória,");
        System.out.println("acorda em Dagobah e busca respostas.\n");
        System.out.print("\nOlá querido(a) Padawan, por favor digite seu nome: ");
        nome=rpg.nextLine();
        
        System.out.println("=NÍVEL 1- DESCOBRIMENTO=\n");
        System.out.println("\n _   _ _           _   __ \n" +
" | \\ | (_)         | | /_ |\n" +
" |  \\| |___   _____| |  | |\n" +
" | . ` | \\ \\ / / _ \\ |  | |\n" +
" | |\\  | |\\ V /  __/ |  | |\n" +
" |_| \\_|_| \\_/ \\___|_|  |_|");
        System.out.println("\n\nVocê acorda em sua X-Wings, observa pela janela e se\n assusta pelo fato"
                + " de estar em Dagobah, sozinho, sem seu mestre Skywalker, \ndecide procurar Luke,"
                + " você tem alguns flashes de memória do que houve e como\n chegou em Dagobah, "
                + "e sente medo do pouco que lembra. ");
        System.out.println("Aperte [ENTER] para continuar");
        rpg.nextLine();
        
        System.out.println("\n\nQuerido(a) Padawan, decida entre qual dos lados quer seguir:"
                + "\n1 - Montanhas."
                + "\n2 - Rio.");
        int toma = rpg.nextInt();
        
        switch (toma) {
            case 1:
                Montanhas();
                break;
            case 2:
                Rio();
                break;
            default:
                System.out.println("Esta opção não está válida no momento.");
                break;
        }
    } static void Montanhas() {
         System.out.println("\nLuke não se encontra nas Montanhas, escolha entre voltar para:"
                    + "\n1 - Para voltar para nave."
                    + "\n2 - ir para o rio.");
         int toma = rpg.nextInt();
         
         switch (toma) {
             case 1:
                 Navef1();
                 break;
             case 2:
                 Rio();
             default:
                 System.out.println("Está opção não está válida no momento.");
                break;
         }
    } static void Navef1(){
         System.out.println("\nJovem Padawan, escolha entre:\n1-ir embora\n2-seguir em direção "
                    + "ao Rio");
            int toma = rpg.nextInt();
            
            switch (toma) {
                case 1:
                    System.out.println("\nGAME OVER\nVocê, jovem Padawan, está fugindo do seu dever");
                    morre();
                    break;
                case 2:
                    Rio();
                    break;
                default:
                    System.out.println("Esta opção não é valida no momento.");
                    System.exit(0);
                    break;
            }
    } static void Rio(){
            System.out.println("Aperte [ENTER] para continuar");
            rpg.nextLine();
        System.out.println("\nChegando ao Rio, percebe que Luke não se encontra em lugar "
                            + "\nnenhum, logo a frente, observa uma forma de vida, se aproxima mais e "
                            + "\npercebe que é Obi Wan, o Mestre Jedi diz: estava a sua espera e "
                            + "\nlhe entrega um holograma, neste holograma falava:");
                    
        System.out.println("\n\n“Olá "+ nome +" deixo a você esse holograma para testar seus limites com esses desafios, após completá-los terá tudo para encontrar o que procura.\n");
                 System.out.println("Pressione [ENTER] para prosseguir.");
                 rpg.nextLine();
               System.out.println("      1- Não encontrará nada neste planeta.\n" +
                            "                 2- O próximo planeta que deverá se aventurar será? \n" +
                            "Foi apresentado pela primeira vez em 2015 no filme Star Wars: o despertar da força.\nÉ o planeta desértico localizado em uma seção remota do Extensões Ocidentais.\n" +
                            "Apresenta um lugar semelhante a um grande deserto de areia e dunas enormes\nAlternativas: \n" +
                            "1- Alderaan \n" +
                            "2- Akiva \n" +
                            "3- Shili\n" +
                            "4- Jakku \n" +
                            "5- Jedha");
                            int planeta = rpg.nextInt();
                            
                            switch (planeta){
                                case 4:
                                     System.out.println("=Nível 2 DESBLOQUEADO=\nO HOLOGRAMA SE ENCONTRA NO "
                            + "INVENTÁRIO");
                                     fase02();
                                     break;
                                default:
                                   System.out.println("\nGAME OVER. QUE A FORÇA ESTEJA COM VOCÊ."
                + "\n\nJogo desenvolvido pelo grupo-05 BSI:"
                + "\nDaniel Kudo"
                + "\nKariane Coura"
                + "\nPedro Uemura"
                + "\nPhellype Guilherme"
                + "\n\nEsperamos que tenha gostado.");
                                    System.exit(0);
                                    break;
                            }
    }

   static void fase02 () {

//nome eh a string do nome da pessoa
//AGORA A PESSOA POSSUI UM CHECKPOINT
 
   System.out.println("\n _   _ _           _   ___  \n" +
" | \\ | (_)         | | |__ \\ \n" +
" |  \\| |___   _____| |    ) |\n" +
" | . ` | \\ \\ / / _ \\ |   / / \n" +
" | |\\  | |\\ V /  __/ |  / /_ \n" +
" |_| \\_|_| \\_/ \\___|_| |____|\n");
        System.out.println("Conquista desbloqueada == SABRE DE LUZ");
        System.out.println("\nVocê chega em Jakku e estaciona sua X-Wings, nota-se que perto há uma grande tropa de stormtroopers."
                + "\nEles avistam sua nave e vão em sua direção!!"
                + "\nInfelizmente um deles acaba acertando um dos propulsores de sua nave e não há como voar."
                + "\n\nPadawan, decida entre FUGIR de sua nave e se esconder ou pegar o seu sabre de luz no inventário e LUTAR bravamente" ); 
        String decisao1 = rpg.next();
    while (!decisao1.equalsIgnoreCase("lutar")){
            System.out.println("\n\nVocê tentou se esconder mas ao correr para atrás de uma Árvore, apareceu um AT-ST e você foi morto. "
            + "\nGAME OVER");
            System.out.println("\nÚLTIMO CHECKPOINT" 
                    + "\nPadawan, decida entre FUGIR de sua nave e se esconder ou pegar o seu sabre de luz no inventário e LUTAR bravamente");
            decisao1 = rpg.next();
            }
            if (decisao1.equalsIgnoreCase("lutar")){
            System.out.println("\n\nTodos os stormtroopers estão vindo!!"
                    + "\nPara pegar o Sabre de luz digite SABRE + ENTER");
            }
            int energia = 100,ataque = 25, vida = 100;
            String pegar = rpg.next();
            if(pegar.equalsIgnoreCase("sabre")){
                    System.out.println("\n\nVocê pegou o Sabre!!"
                    + "\nPara atacar digite: ATACAR + ENTER!!"
                    + "\nVida: " + vida
                    + "\nEnergia: " + energia 
                    + "\nDano de Ataque: " + ataque);
            }
            String atacar = rpg.next();
            if (atacar.equalsIgnoreCase("atacar")){
                System.out.println("\n\nVocê já eliminou 5 stormtroopers!!"
                    + "\nContinue atacando!! {ATACAR+ENTER}"
                    + "\nVida: " + (vida - 25) //75 de vida
                    + "\nEnergia: " + (energia-50) //50 de energia
                    + "\nDano de Ataque: " + ataque);
            }
                String continuar = rpg.next();
            if(continuar.equalsIgnoreCase("atacar")){
                System.out.println("\n\nVocê já eliminou 15 stormtroopers, faltam mais 5!!"
                    + "\nSeja percistente e continue!!"
                    + "\nVida: " + (vida - 50) //50 de vida 
                    + "\nEnergia: " + (energia-75) //25 de energia
                    + "\nDano de Ataque: " + ataque);
            }
                        String continuar2 = rpg.next();
            if(continuar2.equalsIgnoreCase("atacar")){
                System.out.println("\n\nVocê eliminou todos os stormtrooper, porém está muito ferido!!"
                    + "\nVida: " + (vida - 75) //25 de vida 
                    + "\nEnergia: " + (energia-95) //5 de energia
                    + "\nPara recuperar a vida digite (VIDA + ENTER) e para recuperar energia digite (ENERGIA + ENTER) ");
            String vidaouenergia = rpg.next();
            if (vidaouenergia.equalsIgnoreCase("vida")){
                    System.out.println("\n\nVocê se curou!!"
                    + "\nVida: " + vida//100 de vida
                    + "\nEnergia: " + (energia -95)    //5 de energia    
                    + "\nPara recuperar energia digite ENERGIA + ENTER");
            
                    String energia2 = rpg.next();
                    if (energia2.equalsIgnoreCase("energia")){
                        System.out.println("\n\nVocê já está pronto!! "
                                + "\nVida: 100"
                                + "\nEnergia: 100");
                        System.out.println( "\nJovem Padawan, no momento você se encontra em um deserto no planeta Saturno"
                        + "\nDe repente, de longe, escuta uma voz bem baixinho.");
            
            System.out.println("\nPadawan decida entre: \n"
                                + "\n1 - seguir a voz."
                                + "\n2 - seguir o holograma.\n");
            }
                
                System.out.println("Sua escolha: ");
                int decisao = rpg.nextInt();
                
                switch (decisao) {
                    case 1:
                        fase03PH();
                        break;
                    case 2:
                        fase03Uemura();
                        break;
                    default:
                        System.out.println("Comando inválido.");
                        break;
        }}
       
            if (vidaouenergia.equalsIgnoreCase("energia")){ 
                    System.out.println("\n\nVocê recuperou sua energia!!"
                        + "\nVida: " + (vida-75) //25 de vida
                        + "\nEnergia: " + energia //enegria 100
                        + "\nPara recuperar a vida digite (VIDA + ENTER) ");
            
                        String energia3 = rpg.next();
                    if (energia3.equalsIgnoreCase("vida")){
                        System.out.println("\n\nVocê já está pronto!! "
                                + "\nVida: 100"
                                + "\nEnergia: 100");
                        System.out.println("\nJovem Padawan, no momento voce se encontra em um deserto no planeta Saturno"
                        + "\nDe repente, de longe, escuta uma voz bem baixinho.");
            
             }      
             System.out.println("\nPadawan decida entre: \n"
                                + "\n1 - seguir a voz."
                                + "\n2 - seguir o holograma.\n");
                
                System.out.println("Sua escolha: ");
                int decisao02 = rpg.nextInt();
                
                switch (decisao02) {
                    case 1:
                        fase03PH();
                        break;
                    case 2:
                        fase03Uemura();
                        break;
                    default:
                        System.out.println("Comando inválido.");
                        break;
   
   }}}
   }
   static void fase03Uemura() {
       
       System.out.println("Você escolheu seu caminho e chegou até aqui, estás próximo do final jovem jedi. Sua busca está por cessar.\n"
                          + "\nUse todo o seu conhecimento adquirido e lute por seus conceitos.\n"
                          + "\nPressione [Enter] para prosseguir para a fase final.");
        rpg.nextLine();
        
        System.out.println(" _   _ _           _    ___ ____  \n" +
                           " | \\ | (_)         | |  / _ \\___ \\ \n" +
                           " |  \\| |___   _____| | | | | |__) |\n" +
                           " | . ` | \\ \\ / / _ \\ | | | | |__ < \n" +
                           " | |\\  | |\\ V /  __/ | | |_| |__) |\n" +
                           " |_| \\_|_| \\_/ \\___|_|  \\___/____/ \n" +
                           "\nVocê chegou a fase 03, " + nome + " você travou uma árdua batalha,"
                           + "\nporém a força é bondosa em quem habita, seus ferimentos e sua energia voltam para: " + vidaPadawan + " pontos.\n\n"
                                + "Como seguem as pistas você deverá encontrar o local onde Luke encontrou Obi Wan pela primeira vez.\n\n"
                                   + "Pressione [ENTER] para prosseguir.");
        rpg.hasNextLine();
    
        System.out.println("Você spawna em sua nave, usa baterias de outros dispositivos inimigos para ressurgir um droid que estava anteriormente abandonado sem carga.\n\n"
                + "- R2D2: priuuu pui... priuuu pruin...");
        
        System.out.println("\nO droid se apresentou, seu nome é R2D2.\n\n"
                + "Deseja comprimentar o droide?:\n"
                + "1 - Se deseja comprimenta-lo."
                + "\n2 - para ignora-lo.");
            
        int comp;
        do {
            System.out.println("\n\nDigite sua escolha (1 ou 2): ");
        } while ((comp = rpg.nextInt())  != 1 && comp != 2);

        switch (comp) {
            case 1:
                System.out.println("\n- Padawan: Olá amiguinho como vai?\n\n"
                        + "- R2D2: priii... bzzss...\n\n"
                        + "Pressione [ENTER] para prosseguir.");
                rpg.nextLine();
                rpg.nextLine();
                break;
            case 2:
                System.out.println("\nVocê ignorou o droide, porém ele irá te acompanhar por toda a jornada, logo se acostume.\n\n"
                        + "Pressione [ENTER] para prosseguir.");
                rpg.nextLine();
                rpg.nextLine();
                break;
            default:
                break;
        }
    
        Nave();
        
    }
    
    static void Nave() {
        
        int escolha;
        
        do {
            System.out.println("\n == Dentro da nave ==\n"
                + "\nVocê está em sua nave, estar em casa é sempre bom, mas deseja fazer algo?\n"
                + "\n1 - Vasculhar nave."
                + "\n2 - Pegar o holograma de Luke."
                + "\n3 - Brincar com o droide."
                + "\n4 - Sair do jogo.");
        
            System.out.println("\nDigite sua escolha:\n");
            escolha = rpg.nextInt();
            
            switch (escolha) {
                case 1:
                    System.out.println("\n\nVocê já vasculhou essa nave milhares de vezes, não há nada novo no momento.\n\n");
                    break;
                case 2:
                    HologramaLuke();
                    break;
                case 3:
                    System.out.println("\n\n-"+nome+": Como você está garoto?"
                            + "\n\n-R2D2: bzsss... pruii..."
                            + "\n\n-Padawan: Bom garoto!!!\n\n");
                    break;
                case 4:
                    System.out.println("Tente novamente, que a força esteja com você.");
                    System.exit(0);
                    break;
                default:
                    System.out.println("Comando inválido.");
                    break; 
            }  
        } while (escolha != 4);
       
    }
    
    static void HologramaLuke() {
        
        System.out.println("\nVocê pegou o holograma de Luke! Desvende o enigma em binário para encontrar mais pistas para continuar sua jornada :)\n"
                           + "\n01100001 01101100 01100100 01100101 01100101 01110010 01100001 01101110 00001010 ");
        
        System.out.println("\nResposta do enigma: ");
        
        rpg.nextLine();
        
        while (rpg.hasNextLine() && !rpg.nextLine().equalsIgnoreCase("aldeeran")){
            System.out.println("\nParece que ainda não encontramos a resposta correta... Vamos tentar um pouco mais...");
        }
        
        System.out.println("\nParece que encontramos a localização do holograma de Luke. Vamos continuar nossa jornada."
                + "\n\nPressione [ENTER] para prosseguir.");
        
        rpg.nextLine();
        
        batalha();
        
    }
     
    static void batalha() {
    
        System.out.println("NO CAMINHO DO PLANETA VOCÊ DETECTA NAVES INIMIGAS, SUA NAVE ESTÁ EM MODO SORRATEIRO."
                + "\nUSE OS SISTEMAS DE ATAQUE DA NAVE PARA VENCER O INIMIGO SEM SER DETECTADO.\n");
        
        int vidaNave = 15;
        
        System.out.println("Vida das tropas inimigas é: " + vidaNave);

        int escolha;
        
        batalha: {
            do {
                String batalhaMenu = "\n1 - Atacar nave (5 de dano)"
                                + "\n2 - Ataque especial (10 de dano)"
                                + "\n3 - Sair da batalha (Game Over)";

                System.out.println(batalhaMenu + "\nDigite sua escolha:");
                escolha = rpg.nextInt();

                switch (escolha){
                    case 1:
                        vidaNave -=5;
                        System.out.println("\nVocê causou 5 de dano à uma das naves inimigas!"
                                        + "\n\nVida da tropa inimiga: " + vidaNave + "\n");

                        if (vidaNave <= 0){
                            System.out.println("Você derrotou todas as naves inimigas! Parabéns!"
                                        + "\n\n=== CONQUISTA DESBLOQUEADA: DESTRUIDOR DE NAVES ===");
                            break batalha;
                        }

                        break;
                    case 2:
                        vidaNave -=10;
                        System.out.println("Você usou o especial e causou 10 de dano a tropa de naves do inimigo."
                                        + "\n\nVida da tropa inimiga: " + vidaNave + "\n");
                        
                        if (vidaNave <= 0) {
                            System.out.println("Você derrotou todas as naves inimigas. Muito bem."
                                        + "\n\n=== CONQUISTA DESBLOQUEADA: DESTRUIDOR DE NAVES ===");
                            break batalha;
                        }
                        
                        break;
                    case 3:
                        System.out.println("VOCÊ É FRACO! TE FALTA ÓDIO.");
                       morre();
                        System.exit(0);
                        break;
                    default:
                        break;
                }

            } while (escolha != 3);
            
        }
        Planeta();
    }
    
    static void Planeta() {
        
        System.out.println("\n\nVocê chegou em Aldeeran. Logo na entrada do planeta, você sente fortes arrepios por todo o corpo. "
                            + "\nEsse planeta mostra uma grande presença de força maligna.\n");
        System.out.println("\nPressione [ENTER] para prosseguir.");
        rpg.nextLine();
        
        System.out.println("\n\n[Planeta Aldeeran]");
        
        System.out.println("\n\nUMA VOZ ENTRA NA SUA CABEÇA, É UMA VOZ ROBÓTICA E OFEGANTE:"
                            + "\n\n- Desconhecido: A força está com você " + nome + " mas você ainda não é um Jedi por completo.\n");
        System.out.println("\nPressione [ENTER] para prosseguir.");
        rpg.nextLine();
        
        System.out.println("\nVocê fica confuso, mas segue seu caminho.");
        
        System.out.println("\nVocê avista dois caminhos, por onde quer seguir?"
                            + "\n\n1- Floresta dos carvalhos."
                            + "\n2- Pântano sombrio.");
        
        int decisao;
        
        do {
            System.out.println("\nSua decisão: ");
            decisao = rpg.nextInt();
            
            switch(decisao) {
                case 1:
                    System.out.println("\nVocê decidiu ir pela Floresta dos carvalhos, o caminho mais difícil."
                                        + "\nTome cuidado grandes perigos aguardam você.");
                    floresta();
                    break;
                case 2:
                    System.out.println("Você decidiu ir pelo pântano sombrio, o caminho mais fácil."
                                        + "Use suas habilidades para sair de toda essa sujeira.");
                    pantano();
                    break;
            }
             
        } while (decisao != 1 || decisao != 2);
    }
    
    static void floresta() {
        
        System.out.println("\n\n[Floresta dos carvalhos]");
        
        System.out.println("\nVocê encontra um Stormtrooper muito bem equipado.\nTerá que enfrentá-lo para prosseguir!"
                            + "\nUse seu sabre de luz para aniquilar o inimigo.");
        
        lutafloresta();
    }
    
    static void lutafloresta(){
        
        System.out.println("\n[Luta]");
        
        System.out.println("\n[Sua vida é: " + vidaPadawan + "]");
        System.out.println("\n[Vida do StormTrooper: " + vidaSTE + "]");
        
        boolean venceu = false;
        int decisao;
        
        do {
            System.out.println("\nO que irá fazer:"
                    + "\n1 - Atacar."
                    + "\n2 - Fugir. (Game Over).");
            
            System.out.println("\nEscolha:");
            decisao = rpg.nextInt();
            
            if (decisao == 1) {
                venceu = atacarSTE();
            } else if (decisao == 2) {
                morre();
            }
        } while (decisao != 2 && !venceu);
    }
    
    static boolean atacarSTE() {
        int Damage = 0;
        
        Random random = new Random();
        if (acessorioPlayer01.equals("Sabre de Luz")) {
            Damage = 5;
        }
        
        System.out.println("\nVocê atacou o StormTrooper!");
        System.out.println("\nSeu dano foi: " + Damage);
        
        vidaSTE -= Damage;
        
        System.out.println("Vida do inimigo: " + vidaSTE);
        
        if (vidaSTE < 1) {
            seguircaminho();
            return true; 
        } else if (vidaSTE > 0) {
        int DamageSTE = 0;
        
        DamageSTE = random.nextInt(9);
           
        System.out.println("\nVocê foi atacado pelo StormTrooper de elite.");
        System.out.println("\nVocê tomou: " + DamageSTE);
        
        vidaPadawan -= DamageSTE;
        
        System.out.println("Vida Padawan: " + vidaPadawan);
        
        if(vidaPadawan <= 0) {
            morre();
            }
        } return false;
        
    }
    
    static void pantano(){
        
        System.out.println("\n\n[Pântano sombrio]");
        
        System.out.println("\nVocê encontrou um bando de Stormtrooper que aparentam estar despreparados.\nTerá que enfrentá-los para prosseguir!"
                            + "\nUse seu sabre de luz para aniquilar o inimigo.");
        
        lutafloresta();
    }
    
    static void lutapantano(){
        
        System.out.println("\n[Luta]");
        
        System.out.println("\n[Sua vida é: " + vidaPadawan + "]");
        System.out.println("\n[Vida dos StormTroopers: " + vidaTropas + "]");
        
        boolean venceu = false;
        int decisao;
        
        do {
            System.out.println("\nO que irá fazer:"
                    + "\n1- Atacar."
                    + "\n2- Fugir. (Game Over).");
            
            System.out.println("\nEscolha:");
            decisao = rpg.nextInt();
            
            if (decisao == 1) {
                venceu = atacarTropas();
            } else if (decisao == 2) {
                morre();
            }
        } while (decisao != 2 && !venceu);
    }
    
    static boolean atacarTropas() {
        int Damage = 0;
        
        Random random = new Random();
        if (acessorioPlayer01.equals("Sabre de Luz")) {
            Damage = 8;
        }
        
        System.out.println("\nVocê atacou o StormTrooper!");
        System.out.println("\nSeu dano foi: " + Damage);
        
        vidaTropas -= Damage;
        
        System.out.println("Vida do inimigo: " + vidaTropas);
        
        if (vidaTropas <= 0) {
            seguircaminho();
            return true; 
        } else if (vidaTropas > 0) {
        int DamageTropas = 0;
        
        DamageTropas = random.nextInt(5);
           
        System.out.println("\nVocê foi atacado pelo StormTrooper de elite.");
        System.out.println("\nVocê tomou: " + DamageTropas);
        
        vidaPadawan -= DamageTropas;
        
        System.out.println("Vida Padawan: " + vidaPadawan);
        
        if(vidaPadawan < 1) {
             morre();
            
            }
        } return false;
        
    }
    
    static void seguircaminho(){
        
        System.out.println("\n[Seguindo pela estrada]");
        
        System.out.println("\nParábens você passou no seu desafio e por isso conseguiu o acesso ao uso da força."
                          + "\nUse a força para causar mais dano em inimigos.");
        System.out.println("\n\nPressione [ENTER] para prosseguir.");
        rpg.nextLine();
        rpg.nextLine();
        
        System.out.println("\nA voz em sua cabeça fica cada vez mais forte.\n" +
                       "-Desconhecido: Seu mestre já está morto pequena criatura e você virará meu servo.");
        System.out.println("\n\nPressione [ENTER] para prosseguir.");
        rpg.nextLine();
        
        System.out.println("\n- R2D2: pipopipopipo");
        
        System.out.println("             ______             \n" +
"          ,-'//__\\\\`-.          \n" +
"        ,'  ____      `.        \n" +
"       /   / ,-.-.      \\       \n" +
"      (/# /__`-'_| || || )      \n" +
"      ||# []/()] O || || |      \n" +
"    __`------------------'__    \n" +
"   |--| |<=={_______}=|| |--|   \n" +
"   |  | |-------------|| |  |   \n" +
"   |  | |={_______}==>|| |  |   \n" +
"   |  | |   |: _ :|   || |  |   \n" +
"   > _| |___|:===:|   || |__<   \n" +
"   :| | __| |: - :|   || | |:   \n" +
"   :| | ==| |: _ :|   || | |:   \n" +
"   :| | ==|_|:===:|___||_| |:   \n" +
"   :| |___|_|:___:|___||_| |:   \n" +
"   :| |||   ||/_\\|| ||| -| |:   \n" +
"   ;I_|||[]_||\\_/|| ||| -|_I;   \n" +
"   |_ |__________________| _|   \n" +
"   | `\\\\\\___|____|____/_//' |   \n" +
"   J : |     \\____/     | : L   \n" +
"  _|_: |      |__|      | :_|_  \n" +
"-/ _-_.'    -/    \\-    `.-_- \\-\n" +
"/______\\    /______\\    /______\\");
        
        System.out.println("\n\nPressione [ENTER] Para prosseguir.");
        rpg.nextLine();
        
        System.out.println("Após passar a batalha você se depara com a força maligna crescendo mais e mais,\n"
                + "porém no fundo sente a presença de seu mestre Luke Skywalker!\n"
                + "É como se o seu sangue borbulhasse. De longe você avista uma base inimiga.");
        System.out.println("\n\nPressione [ENTER] Para prosseguir.");
        rpg.nextLine();
        
        base();
    }
    
    static void base(){
        
        System.out.println("Chegando a base: você depara com uma cerca de lasers então pede para o R2D2 destravá-la.\n"
                           + "\nEscreva: [R2D2 destrave+[ENTER]] para prosseguir");
        
        System.out.println("\nDigite para seguir: ");
        
        while (!rpg.nextLine().equalsIgnoreCase("R2D2 destrave")){
            System.out.println("\nParece que ainda não encontramos a resposta correta...\nVamos tentar um pouco mais...");
        }
        
        System.out.println("        .=.\n" +
"       '==c|\n" +
"       [)-+|\n" +
"       //'_|\n" +
"  ... /]==;\\");
        System.out.println("\nVocê destravou a porta."
                + "\n\nPressione [ENTER] para prosseguir.");
        
        rpg.nextLine();
        
        System.out.println("Você se depara com uma presença massiva,"
                + "\nquando olha para o lado vê um bocado de StormTrooper mortos."
                + "\n\nVê duas pessoas vindo em sua direção.");
        System.out.println("\nPressione [Enter] para prosseguir.");
        
        rpg.nextLine();
        
        int decisao;
        do {
            
            System.out.println("\nA presença de Luke é automaticamente confirmada, você sente isso cada vez mais forte.\n");
            System.out.println("1 - Para se aproximar.");
            System.out.println("\n2- Para se afastar.");
            decisao = rpg.nextInt();
            
            if (decisao == 1){
                System.out.println("\n Você se aproxima, tome cuidado, o poder maligno está muito forte.");
                Final();
            } else if (decisao == 2){
                System.out.println("\n Você até tenta se afastar mas é como se seus pensamentos e corpo estivessem sendo puxados pela força.");
                Final();
            }
        }while (decisao != 2 || decisao != 1);
    }
    static void Final() {
        System.out.println("                       .-.\n" +
"                      |_:_|\n" +
"                     /(_Y_)\\\n" +
"                    ( \\/M\\/ )\n" +
" '.               _.'-/'-'\\-'._\n" +
"   ':           _/.--'[[[[]'--.\\_\n" +
"     ':        /_'  : |::\"| :  '.\\\n" +
"       ':     //   ./ |oUU| \\.'  :\\\n" +
"         ':  _:'..' \\_|___|_/ :   :|\n" +
"           ':.  .'  |_[___]_|  :.':\\\n" +
"            [::\\ |  :  | |  :   ; : \\\n" +
"             '-'   \\/'.| |.' \\  .;.' |\n" +
"             |\\_    \\  '-'   :       |\n" +
"             |  \\    \\ .:    :   |   |\n" +
"             |   \\    | '.   :    \\  |\n" +
"             /       \\   :. .;       |\n" +
"            /     |   |  :__/     :  \\\\\n" +
"           |  |   |    \\:   | \\   |   ||\n" +
"          /    \\  : :  |:   /  |__|   /|\n" +
"          |     : : :_/_|  /'._\\  '--|_\\\n" +
"          /___.-/_|-'   \\  \\\n" +
"                         '-'\n");
        
        vidaPadawan = 100;
        
        System.out.println("\n- Darth Vader: Vejo que chegou meu jovem. Hoje eu exterminarei a raça Jedi do multiverso.");
        System.out.println("\nSeu mestre está a beira da morte. Mal sabe ele que todo o esforço de não me contar onde você estava foi em vão."
                           + "\n\n Pobre Luke...");
        
        System.out.println("Pressione [ENTER] para prosseguir.");
        rpg.nextLine();
        
        System.out.println("\nParece que uma luta com Darth Vader é inevitável, o que você deseja fazer?");
        System.out.println("\n1 - Lutar."
                            + "\n2 - Fugir.");
        int decisao = rpg.nextInt();
        
        switch (decisao) {
            case 1:
                batalhaFinal();
                break;
            case 2:
                System.out.println("\nVocê fugiu e morreu.");
               morre();
        System.exit(0);
                
            default:
                break;
        }
        
    }
    static void batalhaFinal(){
        System.out.println("\nX-X-X-X-X-x");
        System.out.println("V工刀丹 ㄗ丹刀丹山丹れ: " + vidaPadawan);
        System.out.println("V工刀丹 刀丹尺匕卄 V丹刀モ尺: " + vidaDV);
        System.out.println("X-X-X-X-X-x");
        
            System.out.println("1 - Atacar com sabre de luz: " + poderSabre + " pontos de dano.");
            System.out.println("\n2 - Atacar com a força: " + poderForca + " pontos de dano.");
            System.out.println("\n3 - Fugir (Game over)");
            int decisao = rpg.nextInt();
            
            switch (decisao) {
                case 1:
                ataquesabre();
                break;
                case 2:
                ataqueforca();
                break;
                case 3:
                System.out.println("Você decidiu fugir e por isso perdeu.");
                 System.out.println("\nGAME OVER. QUE A FORÇA ESTEJA COM VOCÊ."
                + "\n\nJogo desenvolvido pelo grupo-05 BSI:"
                + "\nDaniel Kudo"
                + "\nKariane Coura"
                + "\nPedro Uemura"
                + "\nPhellype Guilherme"
                + "\n\nEsperamos que tenha gostado.");
                 System.exit(0);
                break;
                default:
                break;
        }
    }
    static void ataquesabre() {
        System.out.println("\nVocê atacou Darth Vader com seu sabre de luz: ");
                    vidaDV = vidaDV - poderSabre;
                    
                    System.out.println("\nDarth Vader tomou" + poderSabre + " de dano.");
                    
    if(vidaDV < 1){
                    System.out.println("\nVocê acabou com ele!");
                    Finaldevez();
    }else{
                    System.out.println("\nVocê tomou " + damageDV + " de dano.");
                    vidaPadawan = vidaPadawan - damageDV;

    if(vidaPadawan <= 0 ){
      morre();
    }
    else{
        batalhaFinal();
            }
        }
    }
    static void ataqueforca(){
                    System.out.println("\nVocê atacou Darth Vader usando a força: ");
                    vidaDV = vidaDV - poderForca;
                    
                    System.out.println("\nDarth Vader tomou " + poderForca + " de dano.");
                    
    if(vidaDV <= 0){
                    System.out.println("\nVocê acabou com ele!");
                    Finaldevez();
    }else{
                    System.out.println("\nVocê tomou " + damageDV + " de dano.");
                    vidaPadawan = vidaPadawan - damageDV;
                    
        if(vidaPadawan <= 0 ){
      morre();
    }
    else{
        batalhaFinal();
            }
        }
    }
   
    
    static void Finaldevez(){
        System.out.println("\nVocê derrotou o Darth Vader, salva seu mestre e saia como um Jedi formado pela vida.");
        System.out.println("\nPressione [ENTER] para continuar...");
        rpg.nextLine();
        
        System.out.println("         _.-'~~~~~~`-._\n" +
"        /      ||      \\\n" +
"       /       ||       \\\n" +
"      |        ||        |\n" +
"      | _______||_______ |\n" +
"      |/ ----- \\/ ----- \\|\n" +
"     /  (     )  (     )  \\\n" +
"    / \\  ----- () -----  / \\\n" +
"   /   \\      /||\\      /   \\\n" +
"  /     \\    /||||\\    /     \\\n" +
" /       \\  /||||||\\  /       \\\n" +
"/_        \\o========o/        _\\\n" +
"  `--...__|`-._  _.-'|__...--'\n" +
"          |    `'    |");
        
        System.out.println("\n\nA cabeça de Darth Vader ainda paira sobre o chão caída pelo seu sabre.");
        System.out.println("\n-Luke: Você conseguiu " + nome + ", hoje você me superou.");
        System.out.println("\n-R2D2: pipiropapa...");
        
        System.out.println("   ______________________________________________________________________\n" +
"  |:..                                                      ``:::%%%%%%HH|\n" +
"  |%%%:::::..                    VOCÊ VENCEU.                    `:::::%%%%|\n" +
"  |HH%%%%%:::::....._______________________________________________::::::|\n" +
"\n" +
"            ________   ___   ____\n" +
"           / __   __| / _ \\ |  _ \\\n" +
"     ______> \\ | |   |  _  ||    /_____________________________\n" +
"    / _______/ |_|   |_| |_||_|\\______________________________ \\\n" +
"   / /                                                        \\ \\\n" +
"  | |                                                          | |\n" +
"  | |      A procura do mestre:                                | |\n" +
"  | |                                                          | |\n" +
"  | |                                                          | |\n" +
"  | |      Fase 01: Kariane Coura                              | |\n" +
"  | |      Fase 02: Daniel Kudo                                | |\n" +
"  | |      Fase 03.1: Phellype Guilherme                       | |\n" +
"  | |      Fase 03.2: Pedro Uemura                             | |\n" +
"  | |                                         Continua...      | |\n" +
"   \\ \\____________________________    _   ___   ____   _______/ /\n" +
"    \\___________________________  |  | | / _ \\ |  _ \\ / _______/\n" +
"                                | |/\\| ||  _  ||    / > \\        LS\n" +
"                                 \\_/\\_/ |_| |_||_|\\_\\|__/\n");
 System.out.println(nome+", você descobrirá que muitas das verdades às quais nos prendemos dependem do nosso ponto de vista.");
        System.exit(0);
   }
    
    static void fase03PH() {
            Star();
        }     
        
      
            static void Star() {
            System.out.println("Você escolheu seu caminho e chegou até aqui, estás próximo do final jovem jedi. Sua busca está por cessar.\n"
                          + "\nUse todo o seu conhecimento adquirido e lute por seus conceitos.\n"
                          + "\nPressione [Enter] para seguir para a fase final.");
        rpg.nextLine();
        
        System.out.println(" _   _ _           _    ___ ____  \n" +
                           " | \\ | (_)         | |  / _ \\___ \\ \n" +
                           " |  \\| |___   _____| | | | | |__) |\n" +
                           " | . ` | \\ \\ / / _ \\ | | | | |__ < \n" +
                           " | |\\  | |\\ V /  __/ | | |_| |__) |\n" +
                           " |_| \\_|_| \\_/ \\___|_|  \\___/____/ \n" +
                           "\nVocê chegou a fase 03, " + nome + " você travou uma árdua batalha,"
                           + "\nporém a força é bondosa em quem habita, seus ferimentos e sua energia voltam para: " + vida + " pontos.\n\n"
                                + "Como seguem as pistas você deverá encontrar o local onde Luke encontrou Obi Wan pela primeira vez.\n\n"
                                   + "Pressione [ENTER] para prosseguir.");
                         rpg.hasNextLine();
    
          
          System.out.println("\n[Menu jogador]\n");
          System.out.println("Jogador = " + nome +"\n");
          System.out.println("Vida = 100v\n");
          System.out.println("Inventario = Sabre de luz\n ");
          System.out.print("\nPressione [ENTER] para prosseguir.");
          rpg.nextLine();
          rpg.nextLine();
          
          
          
          System.out.println("Ao seguir a voz que estava bem distante de seus ouvidos, "
                        + "o jovem se depara com aquela imensidão de areia e o frio congelante!");
          
          
          System.out.println("\nComo estava de noite, você se vê olhando para a galáxia.... .\n" );
          
          System.out.println(".         _  .          .          .    +     .          .          .      .\n" +
"        .(_)          .            .            .            .       :\n" +
"        .   .      .    .     .     .    .      .   .      . .  .  -+-        .\n" +
"          .           .   .        .           .          /         :  .\n" +
"    . .        .  .      /.   .      .    .     .     .  / .      . ' .\n" +
"        .  +       .    /     .          .          .   /      .\n" +
"       .            .  /         .            .        *   .         .     .\n" +
"      .   .      .    *     .     .    .      .   .       .  .\n" +
"          .           .           .           .           .         +  .\n" +
"  . .        .  .       .   .      .    .     .     .    .      .   .\n" +
"\n" +
" .   +      .          ___/\\_._/~~\\_...__/\\__.._._/~\\        .         .   .\n" +
"       .          _.--'                              `--./\\          .   .\n" +
"           /~~\\/~\\                                         `-/~\\_            .\n" +
" .      .-'                                                      `-/\\_\n" +
"  _/\\.-'                                                          __/~\\/\\-.__\n" +
".'                                                                           `.dp");
        System.out.print("\nPressione [ENTER] para prosseguir.");
          rpg.nextLine();      
          
          System.out.println("\nCom isso começa um tremende! tempeste de areia....., no local! \n");
          
          decisão();
            }
          
          static void decisão(){
           
          System.out.println("\n 1 - Seguir em frente, para encontrar a origem da voz, que ainda te chama.. " );  
          System.out.println("\n 2 - Parar, sentar no chão do deserto naquele frio e esperar a tempestade passar! "); 
          System.out.println("\n 3 - Tentar voltar, no meio da tempestada!  "); // 
          System.out.println("\n 4 - Sair do jogo");
          System.out.print("\nDigite sua escolha:\n");
          
          
          escolha = rpg.nextInt();
          
             
                switch (escolha) {
                    case 1:
                        System.out.println(" \n Nesta bela jornada " + nome +  ", jovem padawan, seguindo a voz que está cada vez mais próxima!\n"
                                + "\nEncontra-se andando sozinha naquela imensidão\n");
                        SEGUIRVOZ();
                        
                        break;
                    case 2:
                        System.out.println("Você decide ficar sentado, esperando o tempo passar.\n");
                                sentado();
                        break;
                    case 3:
                        System.out.println("Você decide voltar e parar de seguir aquela voz "
                                + "\ne continuar sua viagem pelo holograma!");
                        fase03Uemura();
                        break;
                     
                    case 4:
                        morre();
                        
                    default:
                        System.out.println("Comando inválido");
                        decisão();
                        break;
                }
          
          
          }
                    
                    static void sentado(){
                        dano = vida - 60;
                        
                    
                        System.out.println("\n A tempestade está cada vez, "
                                + "\nmais forte e com alta velocidade do vento.\n ");
                                
                                
                        System.out.println("Com isso, jovem padawan, acabou vindo voando um pedra "
                                + "e acerta sua cabeça, você acaba desmaindo!"
                                + "[DANO  -60v de vida]");
                                
                        System.out.println("\nvida atual: " + dano);
                              
                        System.out.print("\nPressione 2x[ENTER] para prosseguir.");
                        rpg.nextLine();  
                        rpg.nextLine(); 
                        
                        
                        System.out.println("\nAo acordar você repara que a tempestade já passou..\n");
                        
                        
                        System.out.print("\nPressione 2x[ENTER] para prosseguir.");
                        rpg.nextLine(); 
                        rpg.nextLine();  
                        
                         
                         
                       System.out.println(" \nOlhando para o lado, um ser em pé está parado, "
                               + "\nolhando para você, com olhos gigantes...");
                       
                        System.out.print("\nPressione 2x[ENTER] para prosseguir.");
                        rpg.nextLine(); 
                        rpg.nextLine();  
                        
                       
                       
                       System.out.println("     .;;;.   .;;;.\n" +
"              .;;;.  `:::'  .;;;.\n" +
"            .;',:.`;.`;;;'.;'.:.`;.\n" +
"          .;' .:|:. `;;.;;' .:|:. `;.\n" +
"         .;'  `:|:'  .;;;.  `:|:'  `;.\n" +
"         ;;    `:' .;;o o;;. `:'    ;;\n" +
"         `;;     .;;'_.-._`;;.     ;;'\n" +
"           `;;..;':. '.-.' .:`;..;;'\n" +
"              `'   `:.   .:'   `'\n" +
"          MJP        `;\";'\n" +
"               .;;;..;: :;..;;;.\n" +
"             .;'               `;.\n" +
"            .;'  .;.       .;.  `;.\n" +
" .;`;.     .;'  .;' `;   ;' `;.  `;.     .;';.\n" +
" ;  ;`;. .;' .;'    .;   ;.    `;. `;. .;';  ;\n" +
"  `'`; `;..;'       ;;   ;;       `;..;' ;'`'\n" +
"   .;'   `;         ;;. .;;         ;'   `;.\n" +
" .;' ;'.; `;.       ;;;;;;;       .;' ;.`; `;.\n" +
";' .-.   `. `;     .;;' ';;.     ;' .'   .-. `;\n" +
"`:_).'    ( :'    ;;;'   `:::    `: )    `.(_:'\n" +
"                  `;;     ;;'\n" +
"                   (;     ;)\n" +
"                   ;;.    ;;\n" +
"                   ;;;   ;;;\n" +
"                   ;;'   `;;\n" +
"                   ;'     `;\n" +
"             _____.;       ;._____\n" +
"             )_.-' /       \\ `-._(\n" +
"               ).-'         `-.(");
                       
                       System.out.println("-Ser Estranho: blu bla bla blu blu bli bli blu bli blo blu bli blo bleblu bla\n "
                               + "bla blu blu bli bli blu bli blo blu bli blo ble........\n");
                       
                       
                       System.out.println("Ele acaba pegando seu sabre de luz, no momento que você estava desacordado.");
                       
                        System.out.print("\nPressione [ENTER] para prosseguir.");
                               rpg.nextLine();  
                       
                       
              
                      System.out.println("1 - ir para cimar do monstro e tentar, lutar!) ");
                      System.out.println("2 - Tentar comunicação, com a criatura bizzara!) " );
                      System.out.print("\nDigite sua escolha:\n");
                      escolha = rpg.nextInt();
                      
                      if(vida >= 40){
                      
                            switch (escolha) {
                                case 1:
                                    System.out.println("\nVocê, jovem padawan, vai para cima do ser estranho,"
                                            + "\ncom isso "
                                            + ", ele simplismente consegue utilizar seu sabre de luza, assim atacando você, DANO: [-40v de vida]\n");
                                    int dano2 = dano - 40;
                                    morre();
                                    System.exit(0);
                                case 2:
                                    System.out.print("\nPressione [ENTER] para prosseguir.");
                                    rpg.nextLine();
                                    rpg.nextLine();
                                    System.out.println(nome + ", padawan decide,conversar!");
                                    System.out.println("\n- " + nome + ", seu onkro (lingua nativa de saturno) está um pouco enferrujado"
                                            + "mas você tentar a comunicação....\n");
                                    System.out.print("\nPressione [ENTER] para prosseguir.");
                                    rpg.nextLine();
                                    System.out.println("\n-" + nome +":  blu bla bla blu blu bli bli blu bli blo blu bli blo ble\n");
                                    System.out.println("O monstro acaba se assustanto e sai correndo...\nDeixando seu sabre no chão!");
                                    System.out.println("Você o pega e continua a sua jornada..\n");
                                    System.out.print("\nPressione [ENTER] para prosseguir.");
                                    rpg.nextLine();
                                    System.out.println("\na voz volta a te chamar, e está cada vez mais perto!  ");
                                    break;
                                default:
                                    System.out.println("Comando inválido, o jogo voltou para o ultimo CHECKPOINT....");
                                    sentado();
                                    break;
                            }
                      }
                            
                            
                            SEGUIRVOZ();
                                    
                                  
                            
                            
                    
           
             
         }
          
                    static void SEGUIRVOZ(){
                      System.out.println("\nAo passar a tempestade, o planeta está, praticamente, de dia.\n");
                              
                      
                      System.out.println("\nVocê encontra a origem da voz, você percebe que é uma nave antiga, "
                              + "e está lá há bastante tempo...\n ");
                                    decisão1();}
                    
                      
                     static void decisão1(){
                      System.out.println("\n1 - Tentar entrar pela porta principal da nave!\n");
                      System.out.println("\n2 - Tentar entrar pela porta de carga da nave!\n");
                      System.out.print("\nDigite sua escolha:\n");
                      escolha = rpg.nextInt();
                      
                      
                          switch (escolha) {
                              case 1:
                                  System.out.println("Você tenta abrir a porta pelo display da nave! "
                                          + "\n[ERRO ERRO ERRO porta Principal requer codigo de acesso!\n "
                                          + "\n[NÃO É PÓSSIVEL ENTRAR NA NAVE]\n"
                                          + "\nTente de outro jeito...\n");
                                  decisão1();
                                  break;
                              case 2:
                                  System.out.println("Você, utiliza o poder da Força para abrir a porta de carga.\n");
                                  break;
                                  
                              default:
                                  System.out.println("Comando Inválido!");
                                    SEGUIRVOZ();
                                  break;
                          } 
                               
                      System.out.println("\nEntrando na nave, você descobre a origem da voz!\n");
                      System.out.println("\nA coisa pula com tudo para cima de você, revelando ser,\n");
                      System.out.println(" um droide......");
                      
                        System.out.print("\nPressione 2x[ENTER] para prosseguir.");
                        rpg.nextLine(); 
                       
                        rpg.nextLine(); 
                          
                      
                      System.out.println("\nEle está completamente assustado..\n");
                      System.out.println("Você o chama para perto! ");
                      
                        System.out.print("\nPressione [ENTER] para prosseguir.");
                        rpg.nextLine(); 
                        
                       
                      System.out.println("\n" + nome +", " + "Ola amiguinho, qual é o seu nome?\n");
                      System.out.println("DROID: bbbbbbbbbbbbbbbb.....");
      
                     
                        
                      System.out.println("[Você Pensa]: A força me chamou para essa nave para encontrar somente esse droide?\n");
                      
                      
                      
                       System.out.print("\nPressione [ENTER] para prosseguir.");
                       rpg.nextLine();
                      
  
                      System.out.println("\nAo pensa nisso, olhando para a porta com a poeira do deserto batendo em seu rosto, "
                              + "você percebe que está vindo alguém!\n");
                      
                      System.out.println("- " + nome + ": Quem é?  ");
                      
                      System.out.print("\nPressione [ENTER] para prosseguir.");
                        rpg.nextLine(); 
                       
                    
                    
                      System.out.println("\nAo olhar mais atentamente é uma projeção astral de um ser baixinho e verde, " +
                        "\nentrando pela porta de carga da nave!\n");
                    
                    
                    
                        System.out.print("\nPressione [ENTER] para prosseguir.");
                            rpg.nextLine();
                          
                          
      System.out.print( "      ____\n" +
"                 _.' :  `._\n" +
"             .-.'`.  ;   .'`.-.\n" +
"    __      / : ___\\ ;  /___ ; \\      __\n" +
"  ,'_ \"\"--.:__;\".-.\";: :\".-.\":__;.--\"\" _`,\n" +
"  :' `.t\"\"--.. '<@.`;_  ',@>` ..--\"\"j.' `;\n" +
"       `:-.._J '-.-'L__ `-- ' L_..-;'\n" +
"         \"-.__ ;  .-\"  \"-.  : __.-\"\n" +
"             L ' /.------.\\ ' J\n" +
"              \"-.   \"--\"   .-\"\n" +
"             __.l\"-:_JL_;-\";.__\n" +
"          .-j/'.;  ;\"\"\"\"  / .'\\\"-.\n" +
"        .' /:`. \"-.:     .-\" .';  `.\n" +
"     .-\"  / ;  \"-. \"-..-\" .-\"  :    \"-.\n" +
"  .+\"-.  : :      \"-.__.-\"      ;-._   \\\n" +
"  ; \\  `.; ;                    : : \"+. ;\n" +
"  :  ;   ; ;                    : ;  : \\:\n" +
" : `.\"-; ;  ;                  :  ;   ,/;\n" +
"  ;    -: ;  :                ;  : .-\"'  :\n" +
"  :\\     \\  : ;             : \\.-\"      :\n" +
"   ;`.    \\  ; :            ;.'_..--  / ;\n" +
"   :  \"-.  \"-:  ;          :/.\"      .'  :\n" +
"     \\       .-`.\\        /t-\"\"  \":-+.   :\n" +
"      `.  .-\"    `l    __/ /`. :  ; ; \\  ;\n" +
"        \\   .-\" .-\"-.-\"  .' .'j \\  /   ;/\n" +
"         \\ / .-\"   /.     .'.' ;_:'    ;\n" +
"          :-\"\"-.`./-.'     /    `.___.'\n" +
"                \\ `t  ._  / \n" +
"                 \"-.t-._:'"+ "- ESTRANHO : O medo é o caminho para o lado negro. Treine a si mesmo, "
              + "a deixar partir tudo que teme perder." 
                        + " ...\nO medo leva à raiva, a raiva leva ao ódio e o ódio leva ao sofrimento.\n"); 
                      decisão2();}
                      
                      static void decisão2() {
                      System.out.println("\n== Momento de decisão == ") ;  
                      System.out.println("\n1 - Perguta para o ser: (quem é você ?) ");
                      System.out.println("\n2 - Ir para cima tentar Atacá-lo ! " );
                      System.out.print("\nDigite sua escolha:\n");
                      escolha = rpg.nextInt();
                      
                      
                    switch (escolha) {
                        case 1:
                            System.out.println(" \nSou Yoda..... Fui um Grande Mestre do Alto Conselho Jedi"
                                    + " Durante 800 anos treinei novas gerações de Jedi sempre lutando a favor da República Galáctica.\n");
                                    yoda();
                            break;
                            
                        case 2:
                            System.out.println("\nNão é possivel, atacar um ser de Luz, "
                                    + " \ntente de outro jeito! ");
                                decisão2();
                            break;
                    default:
                        System.out.println("\nComando Inválido");
                            decisão2();
                        break;
                }   
                      
                      }
                  static void yoda() {
                      System.out.println("\n[YODA] Eu posso lhe ajudar meu jovem,COM AQUILO QUE DESEJA....\n ");
                      
                    
                      System.out.println("\n CÓDIGO:"
                              + "01101100 01110101 01101011 01100101\n");
                      
                      System.out.println("\n“Desvendar este enigma, você deve! um heroi e amigo de todos ele é!\n");
                      
                      System.out.print("\nPressione [ENTER] para prosseguir.");
                      rpg.nextLine(); 
                      rpg.nextLine(); 
                  
                      
                      
                      System.out.println(nome + " \nOque é isso meu mestre?\n"
                              + "\n você fica sem resposta de Yoda...\n");
                      
                      System.out.print("ESCREVA SUA RESPOSTA: ");
                      
                      String result = rpg.nextLine();
                        
                      if (result.equalsIgnoreCase("luke")) {
                            System.out.println("\nExato, jovem padawan, agora suba nessa nave e vá até Tatooine 'terra' de seu mestre, " 
                                   + "\npara encontrar o poder supremo da força e  LUKE SKYWALKER...\n "
                                    + "\n[YODA]:que a força esteja com você, adeus... \n");
                               
                            System.out.print("\nPressione [ENTER] para prosseguir.");
                                    rpg.nextLine();

                                    Espaço();}
                      else{
                          System.out.println("RESPOSTA INCORRETA, tente novamente.");
                          yoda();
                      }
                  }
                      
    static void Espaço() {
                   
                          
       System.out.println("\nJunto com você nesta viagem está seu novo amigo, que o poder da força"
               + "te levou até ele!\n");
       
       System.out.println("Voando no espaço e o silêncio toma conta do lugar.... ");
       System.out.println("\nVocê tem a blilhante ideia de batizar seu novo amigo droide!\n,");
       System.out.print("\nNomeie seu amiguinho de viagem :\n ");
       nomeAMG = rpg.nextLine();
       
       System.out.println(nomeAMG + " que nome fofofinho.......ahhh");
       
        System.out.print("\nPressione [ENTER] para prosseguir.");
           rpg.nextLine();
      
           
       System.out.println(" \nSeguindo o enigma entregue pelo mestre Yoda, " +"\nVocê está "
               + "\n a caminho do planeta tatooine, chegando na metade do caminho,\n");
       
       System.out.print("\nPressione [ENTER] para prosseguir.\n");
           rpg.nextLine();
      
       
       System.out.println(" De repente, a Nave começa a apitar e a balançar........");
       System.out.println("[Barulho de emergencia]: pipipipipipipipipipipipipipipipipipipi\n");
       
       
        System.out.print("\nPressione [ENTER] para prosseguir.\n");
           rpg.nextLine();
       
       System.out.println("olhando pela janela.............\n");
                            
                                        
System.out.println("          .                  .          .              .\n" +
"       +.           _____  .        .        + .                    .\n" +
"   .        .   ,-~\"     \"~-.                                +\n" +
"              ,^ ___         ^. +                  .    .       .\n" +
"             / .^   ^.         \\         .      _ .\n" +
"            Y  l  o  !          Y  .         __CL\\H--.\n" +
"    .       l_ `.___.'        _,[           L__/_\\H' \\\\--_-          +\n" +
"            |^~\"-----------\"\"~ ^|       +    __L_(=): ]-_ _-- -\n" +
"  +       . !                   !     .     T__\\ /H. //---- -       .\n" +
"         .   \\                 /               ~^-H--'\n" +
"              ^.             .^            .      \"       +.\n" +
"                \"-.._____.,-\" .                    .\n" +
"         +           .                .   +                       .\n" +
"  +          .             +                                  .\n" +
"         .             .      .");


System.out.println(" Você avista a temida estrela da morte dos imperias...\n");
    decisão3();
    }
        static void decisão3(){
        System.out.println("== Momento de decisão == \n") ;       
        System.out.println("1 -  Ir para a estrela da morte. "); // estrela da morte
        System.out.println("2 -  Seguir em frete, pelos asteroides, sem ser visto."); // estrela da morte
        System.out.println("3 - WTF? "); // morte
        System.out.print("\nDigite sua escolha:\n");

        
       
            escolha = rpg.nextInt();
                
                 switch(escolha) {
                     
                    case 1:
                         estrela();
                        break;
                       
                    case 2:
                         tatoine();
                      
                         break;
                         
                    case 3:
                        System.out.println("Você simplesmente pulou na nave em movimento com medo da estrela da morte" +
                               "\n Você MORREU\nQue a força esteja com você. ");
                                   morre();
                        break;
                               
                    
                 }
                        
                      
        } 
                static void estrela(){
                    System.out.println("Entrando na estrela da morte pelo compartimento de carga, "
                            + "\nvocê é visto por um stormtrooper que estava sozinho no local! "
                            + "\nO mesmo sai correndo para tentar avisar a todos..");
                    decisão4();
                    
                }
        
                static void decisão4(){
                     
                     System.out.println("\n1 - Deixar Fugir e avisar a todos assim compromentendo sua jornada! ");
                     System.out.println("\n2 - Atacar o stormtrooper!" );
                     System.out.print("\nDigite sua escolha:\n");
                     
                     escolha = rpg.nextInt();
                     
                     switch(escolha){
                         case 1:
                             System.out.println("Você deixa o stormtrooper fugir, assim ele avisa  a todos ");
                             batalhaestrela();
                             break;
                        case 2:  
                            System.out.println("\nVocê ataca o stormtrooper, assim chamando a atenção de todos os inimigos "
                           + "que estavam por perto em outra cabine!");
                            batalhaestrela();
                            
                     }
                    
                }
                    

    
              static void batalhaestrela(){
               
                  
            
            System.out.println("  "
                    + "_____                     .-.\n" +
"                      |_:_|\n" +
"                     /(||||\\\n" +
"                    ( |||||/ )\n" +
" '.               _.'-/'-'\\-'._\n" +
"   ':           _/.--'[[[[]'--.\\_\n" +
"     ':        /_'  : |::\"| :  '.\\\n" +
"       ':     //   ./ |oUU| \\.'  :\\\n" +
"         ':  _:'..' \\_|___|_/ :   :|\n" +
"           ':.  .'  |_[___]_|  :.':\\\n" +
"            [::\\ |  :  | |  :   ; : \\\n" +
"             '-'   \\/'.| |.' \\  .;.' |\n" +
"             |\\_    \\  '-'   :       |\n" +
"             |  \\    \\ .:    :   |   |\n" +
"             |   \\    | '.   :    \\  |\n" +
"             /       \\   :. .;       |\n" +
"            /     |   |  :__/     :  \\\\\n" +
"           |  |   |    \\:   | \\   |   ||\n" +
"          /    \\  : :  |:   /  |__|   /|\n" +
"          |     : : :_/_|  /'._\\  '--|_\\\n" +
"          /___.-/_|-'   \\  \\\n" +
"                         '-'\n");

            
            System.out.println("\nKylo Ren,aparece... WTFFFFFFFFFFFFFFF....... \n");
            
              
       
            System.out.println("== Momento de decisão == \n") ;  
            System.out.println("1 - Atacar Kylo Ren!" + " Vida atual: " + vida);
            System.out.println("2 - Fugir.... " + " Vida Kylo Ren: " + inimigo );
            System.out.print("\nDigite sua escolha:\n");
  
            escolha = rpg.nextInt();
            
            switch (escolha) {
                case 1:
                
                    Ataque();
                        
                    break;
                case 2:
                
                    System.out.println("Você decide fugir, correndo voltando para nave...");
                      
                    System.out.print("\nPressione 2X[ENTER] para prosseguir.");
                    rpg.nextLine();
                    rpg.nextLine();
                     
                        tatoine();
                
                default:
                     System.out.println("Comando inválido, o jogo voltou para o ultimo CHECKPOINT....");
                     batalhaestrela();
                    break;
        }
    }
         static void Ataque() {
       
             System.out.println("\nVocê atacou, Kylo Ren com seu sabre!\n ");
                    inimigo = inimigo - Sabre;
                    
                    System.out.println("\n Kylo Ren perdeu " + Sabre + " de Vida.\n");
                    
                    System.out.println("\n Vida atual Kylo: "  + inimigo);
                    
                    
                    
                     System.out.print("\nPressione [ENTER] para prosseguir.");
                     rpg.nextLine();
                     rpg.nextLine();
                    
                    
                     
                     if(inimigo < 1){
                   
                    System.out.println("\nKylo com o ultimo sopro de vida, consegue utilizar o poder de força, e jogá-lo para fora da nave...\n");
                    System.out.print("\nPressione [ENTER] para prosseguir.");
                    rpg.nextLine();
                    morre();
                    
                     
                     } 
                     
                     else{
                         
                     dano = dano + 20 ;
                    System.out.println("\nVocê tomou " + dano+ " de dano.");
                    vida = vida - dano;
                    
                    System.out.println("Sua vida atual: " + vida);

                    
                    if(vida <= 20 ){
                            System.out.println("Você, perdeu muita vida e sabe que não venceria dessa força do mal!!\n");
                            System.out.println("Então, com isso a melhor forma e fugir!!!");
                            tatoine();
                            
                    }
                    
                                           
            else{
                Ataque();
            }
        }
         }
    
                
        
                      static void tatoine(){
                          
                          
            System.out.println("\nVocê, jovem padawan, consegue escapar "
                              +"da demida estrela da morte, foi por pouco.....\n");
            
            
            System.out.println("\n Você se encontra no espaço sideral, com a rapidez dessa nave velha, "
                     +"agora está a caminhado de Tatooine\n");
            
            
            System.out.print("\nPressione [ENTER] para prosseguir.");
                rpg.nextLine();
                
                System.out.print("   *   .                  .              .        .   *          .\n" +
"  .         .                     .       .           .      .        .\n" +
"        o                             .                   .\n" +
"         .              .                  .           .\n" +
"          0     .\n" +
"                 .          .                 ,                ,    ,\n" +
" .          \\          .                         .\n" +
"      .      \\   ,\n" +
"   .          o     .                 .                   .            .\n" +
"     .         \\                 ,             .                .\n" +
"               #\\##\\#      .                              .        .\n" +
"             #  #O##\\###                .                        .\n" +
"   .        #*#  #\\##\\###                       .                     ,\n" +
"        .   ##*#  #\\##\\##               .                     .\n" +
"      .      ##*#  #o##\\#         .                             ,       .\n" +
"          .     *#  #\\#     .                    .             .          ,\n" +
"                      \\          .                         .\n" +
"____^/\\___^--____/\\____O______________/\\/\\---/\\___________---______________\n" +
"   /\\^   ^  ^    ^                  ^^ ^  '\\ ^          ^       ---\n" +
"         --           -            --  -      -         ---  __       ^\n" +
"   --  __                      ___--  ^  ^                         --  __");
                
System.out.println("\n[CHEGANDO EM TATOOINE]");
    System.out.println("O mundo desolado e de cor bege orbitando um par de estrelas binárias,..\n");
    
    System.out.println("\nAo descer com sua nave no planeta,\n" + nomeAMG);
    
    System.out.print("\nPressione [ENTER]...");
           rpg.nextLine();
           
           
    System.out.println("Vocês encontram o planeta completamente destruído, "
            + "e descobre que a estrela da morte, esté por ali antes de vocês chegarem");
    
      System.out.print("\nPressione [ENTER]...");
           rpg.nextLine();
           
           
        System.out.println("- " + nomeAMG + ": bbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbb");
        
        
         
      System.out.print("\nPressione [ENTER]...");
           rpg.nextLine();
        
        
        System.out.println(" ______\n" +
"                         ___)    (___\n" +
"                      __/     __     \\__\n" +
"                     /     \\_/  \\_/     \\\n" +
"                    /      / \\__/ \\      \\\n" +
"                   |          /\\          |\n" +
"                  /       ---(  )---       \\\n" +
"                 |            \\/            |\n" +
"                 | ........................ |\n" +
"                / ._________/    \\_________. \\\n" +
"               | ./ _________    _________ \\. |\n" +
"               |./ //#/\\###())~~(()###/\\#\\\\ \\.|\n" +
"               |/ //#([])##// ~~ \\\\##([])#\\\\ \\|\n" +
"               | //###\\/##//  ~~  \\\\##\\/###\\\\ |\n" +
"               | \\\\######//   ~~   \\\\######// |\n" +
"                \\             /\\             /                  .^. .^.\n" +
"                 )      __   !II!   __      (                   |~| |~|\n" +
"                /' .___//    !II!    \\\\___. '\\                  |~| |~|\n" +
"               (  ' .__/     [II]     \\__. '  )         __      |~| |~|\n" +
"                \\  '          YY          '  /          \\)\\_    |~| |~|\n" +
"                 \\  '  |   ________   |  '  /            \\~~\\   |~~V~~|\n" +
"                  \\  ' | _/'      '\\_ | '  /              \\~~\\_ |~~|~~~\\\n" +
"                   \\  '|/____________\\|'  /                \\~~~\\~~~~~~~~)\n" +
"                    \\   V___======___V   /                  \\~~~\\~~~~~~/\n" +
"                     \\  V   \\____/   V  /                    \\~~~|~~~~~\\\n" +
"                      \\ V   ~~  ~~   V /                      )~~|~~~~~~)\n" +
"                       \\V  ~~\\~~/~~  V/                       \\~~~~~~~~/\n" +
"                       _V ~~~~\\/~~~~ V_                        \\~~~~~~|\n" +
"                   ___/ V\\____/\\____/V \\_____                   \\~~~~~|\n" +
"                __/ :   V    :  :    V   :  :\\___                |====|\n" +
"              _/' .' .' V  .' .' .'  V .' .' .' .\\_              |.' .|\n" +
"             /:  :  :  :  :  :  :  :  :  :  :  :  :\\             |  : |\n" +
"            /. `. `. `. `. `. `. `. `. `. `. `. `. `\\            |`. `|\n" +
"           /  :  :  :  :  :  :  :  :  :  :  :  :  :  \\           |  : |\n" +
"          / .' .' .' .' .' \\\\  '  // ' .' .' .' .' .' \\          |.' .|\n" +
"         / :  :  :  :  :    ))   ((   :  :  :  :  :  : \\         |  : |\n" +
"        |`. `. `. `. `. `. ((  .  )) . `. `. `. `. `. `.\\        |`. `|\n" +
"        |  :  :  :  :  :    ))   ((   :  :  :  :  :  :  :\\       |  : |\n" +
"       / .' .'  ' .' .' .' ((  '  )) ' .' .' .'  ' .' .' .|      /.' .|\n" +
"      | :  : //  :  :  :    ))   ((   :  :  :   \\\\:  :  : |     |:  : |\n" +
"      |. `. || `. `. `. `. ((  .  )) . `. `. `.  ||`. `. `.\\    | `. `\\\n" +
"     /  :  :||   :  :  :    ))   ((   :  :  :  : ||  :  :  :|   |:  :  |\n" +
"    | .' .' || .' .' .' .' ((  '  )) ' .' .' .'  ||.' .' .' |   | .' .'|\n" +
"    |:  :  :||   :  :  :    ))   ((   :  :  :  : ||  :  :  : \\  |:  :  |\n" +
"   /. `. `. || `. `. `. `. ((  .  )) . `. `. `.  ||\\. `. `. `.\\ | `. `.|\n" +
"  |  :  :  : \\\\  :  :  :  :  :  : _   :  :  :   //  \\:  :  :  :\\|:  :  |\n" +
"  |.' .' .' .'\\\\  .' .' .' . _ ' ._\\ ' .' .' . //|   \\.' .' .' .| .' .'|\n" +
"./:  :  :  :  :\\\\   :  :  : /_  :  \\\\ :  :   _// |    \\ :  :  : |:  :  |\n" +
"|. `. `. `. __ `\\\\_  `. `. // `. `. \\\\______/_/ `|     | `. `. `| `. `.|\n" +
"| :/ :  :  /  |  \\_\\______// :  :  : \\______/  : |     |:  :  : |:  :  |\n" +
".'|.' .' ./   |.' .\\______/.' .' .' .' .' .' .' .|      \\.' .' .' .' .'|\n" +
"  |  :  :|    \\  :  :  :  :  :  :  :  :  :  :  :/        \\ : o   :  :  |\n" +
"`/ `. `. |     |. `. `. `. `. `. `. `. `. `. `.|          | o  `. `. `.|\n" +
"| :  :  /      | :  :  :  :  :  :  :  :  :  :  |          | o :  :  :  |\n" +
"|' .' .|       |' .' .' .' .' .' .' .' .' .' .'|           \\ o .' .' .'|\n" +
"  :  : |       | :  :  :  :  :  :  :  :  :  :  :\\           \\ o  :  :  |\n" +
"`. `. /       /`. `. `. I  `. `. `. `. ` I . `. `\\           \\ oo `  o.|\n" +
"  :  |       /:  :  :  : I   :  :  :  :  I  :  :  \\           \\_ oooo  |\n" +
".' .'|      /' .' .' .'  I .' .' .' .' . I ' .' .' \\            \\_____/\n" +
"  : /      /  :  :  :  : I   :  :  :  : I   :  :  : \\\n" +
"`. |      | `. `. `. `.  I `. `. `. `.  I `. `. `. `.\\\n" +
"  :|      |:  :  :  :  : I   :  H H   : I   :  :  :  :\\\n" +
".' |     /' .' .' .' .' . I ' . H H .'  I .' .' .' .' .\\\n" +
"  :|    |  :  :  :  :  :   I :  H H    I :  :  :  :  :  \\\n" +
"`. |    |`. `. `. `. `. `. I  ` L L `. I  `. `. `. `. `. \\\n" +
"  :|    |  :  :  :  :  :  : I    H H  I  :  :  :_ :  :  : \\\n" +
".' |    |.' .' .' .' .' .' . I ' H H I .' .' .' .\\ .' .' .'\\\n" +
"  :|    |  :  :___  :  :  :   I  H HI :  :  :  :  \\  :  :  :\\\n" +
"`. |    |`. `.|   |. `. `. `.  I H H . `. ` _`. `.|\\. `. `. `|\n" +
"  :|    /  :  |   | :  :  :  :  IH H  :  : | _ :  | \\:  :  : |\n" +
".' |   | .' .'|   |' .' _  .' .' H H ' .'  ||   .'|  \\.' .' .|\n" +
"  :|   |:  :  |   | :  _ |   :   H H  :   //   :  |   | :  : |\n" +
"`. /   | `. `./   |. `. || `. `. H H . ` //  `. `.|   |. `. `|\n" +
"  |    |:  : |    | :  : \\\\  :   H H  :_//  :  :  |   | :  : |\n" +
".'|    / .' .|    /' .' . \\\\  .' H H ' _/ .' .' .'\\   |' .' .|\n" +
"  |   | :  : |   |  :  :   \\\\    H H  :  :  :  :  :|  | :  : |\n" +
"`.|   |. `. `|   |`. `. `.  \\\\_. H H . `. `. `. `. |  |. `. `|\n" +
"  |   | :  :/   |:  :  :  :  \\_  H H  :  :  :  :  :|  | :  : |\n" +
".'|   |' .' |  |' .' .' .' .' .' H H ' .' .' .' .' |  |' .' .|\n" +
"  |   | :  :|  | :  :  :  :  :   H H  :  :  :  :  :|  | :  : |\n" +
"`.|  /`. `. |  |. `. `. `. `. `. `. `. `. `. `. `. |   \\ `. `|\n" +
"  / |:  :  :/  / :  : __  :  :  :  :  :  :  :__   :\\    |  :  \\\n" +
".|  | .' .'|  |.' .' |XX\\' .' .' .' .' .' .'/XX|.' .\\   |.' .'|\n" +
".|  /:  :  |  |  :  :  \\X\\:  :  :  :  :  : /X/ :  :  |  |  :  |\n" +
"`| |. `. `.|  |`. `. `. \\X\\_. `. `. `. `._/X/`. `. `.|  |`. `.|\n" +
".| | :  :  |  |  :  :  : \\XX\\_  :  :  :_/XX/:  :  :  |  |  :  |\n" +
".| |' .' ./   /.' .' .' .' \\XX\\' .' .'/XX/.' .' .' .'|  |.' .'|\n" +
".| | :  :|   |:  :  :  :  :  \\X\\_____/X/ :  :  :  :  |  |  :  |\n" +
"`| |. `. |   | `. `. `. `. `. |XXXXXXX|`. `. `. `. `.|  \\`. `.|\n" +
".| | :  :|   |:  :  :  :  :  :|XX| |XX|  :  :  :  :  |   | :  |\n" +
".| |' .' |   | .' .' .' .' .'  \\ |V| / .' .' .' .' .'|   |' .'|\n" +
".| / :  :|   |:  :  :  :  :  : /\\/ \\/\\:  :  :  :  :  |   | :  |\n" +
"=||`. `./    | `. `. `. `. `. |       |`. `. `. `. `.|   |. `.|\n" +
"~\\|  : |     |:  :  :  :  :  :|       |  :  :  :  :  |   | :  |\n" +
"~~|.' .|      \\.' .' .' .' .' |       |.' .' .' .' .'|    \\ .' \\\n" +
"~~|  : |       | :  :  :  :  :|       |  :  :  :  :  |     \\  : \\\n" +
"~~|`. `|       |. `. `. `. `. |       |`. `. `. `. `.|      \\. `.|\n" +
"_~|  : |        \\:  :  :  :  :|       |  :  :  :  : /        |:  |\n" +
".||.' .|         |.' .' .' .' |       |.' .' .' .' |         |===|\n" +
".||  : \\         |  :  :  :  :|       |  :  :  :  :|         /~~~\\\n" +
"  V\\. `.|        |`. `. `. `. |       |`. `. `. `. |        |~~~~~\\\n" +
"    |===|        |  :  :  :  :|       |  :  :  :  :|        \\~~~~~~)\n" +
"    /~~~\\        |.' .' .' .' |       |.' .' .' .' |         )~~~~/\n" +
"   /~~~~~|        \\ :  :  :  :|       |  :  :  :  /         /~_~~~\\\n" +
"  (~~~~~~/         | `. `. `. |       |`. `. `. `|         |~| |~~~)\n" +
"   \\~~~~(          |:  :  :  :|       |  :  :  : |         |~| |~~/\n" +
"   /~~~_~\\         | .' .' .' |       |.' .' .' .|          V  |~|\n" +
"  (~~~| |~|        |:  :  :  :|       |  :  :  : |             |~|\n" +
"   \\~~| |~|        | #. `. `. `\\     / `. `. `.#`|             |~|\n" +
"    |~|  V        / : #:  : #:  )   ( : #:  : #:  \\            |~|\n" +
"    |~|           )' .# .' #' .(     ) .'#.' .# .'(             V\n" +
"    |~|           \\ : ###### :  )   ( :  ######:  /\n" +
"    |~|           /. `# `. #. `(     ) `.#`. `# `.\\\n" +
"     V            ) : #:  :# :  )   ( :  #  : #:  (\n" +
"                  \\' .# .' .# ./     \\ .# .' .# .'/\n" +
"                   |:# :  :  :|       |  :  :  # |\n" +
"                   | `. `. `. |       |`. `. `. `|\n" +
"                   |:  :  :  :|       |  :  :  : |\n" +
"                   | .' .' .' \\       /.' .' .' .|\n" +
"                   |:  :  :  : |     |:  :  :  : |\n" +
"                  /. `/   |`. `|     | `. |   \\ `.\\\n" +
"                 |  :/     \\ : |     |:  /     \\  :|\n" +
"                 |.'[  ( )  ] .|     | .[  ( )  ]' |\n" +
"                 |  [       ]: |     |: [       ] :|\n" +
"                 |`. \\     /. `|     | `.\\     /`. |\n" +
"                  \\ : \\   |  : |     |:  :|   /:  /\n" +
"                   \\ .' .' .' /       \\.' .' .' ./\n" +
"                    |  :  :  |         | :  :  :|\n" +
"                    |`. `. `.|         |. `. `. |\n" +
"                    |  :  :  |         | :  :  :|\n" +
"                     \\' .' .'|         |' .' .'/\n" +
"                      \\:  :  |         | :  : /\n" +
"                       |`. `.|         |. `. |\n" +
"                       |  :  |         | :  :|\n" +
"                       |.' .'|         |' .' |\n" +
"                       |  :  |         | :  :|\n" +
"                       |`. `.|         |. `. |\n" +
"                      /:  :  |         | :  : \\\n" +
"                     |' .' .'|         |' .' .'|\n" +
"                     | :  :  |         | :  :  |\n" +
"                     |. `. `.|         |. `. `.|\n" +
"                     | :  :  |         | :  :  |\n" +
"                     |' .' .'|         |' .' .'|\n" +
"                    /  :  :  |         | :  :  :\\\n" +
"                   / `. `. `./         \\. `. `. `\\\n" +
"                  / :  :  : |           |:  :  :  \\\n" +
"                 /.' .' _/ .|           | .\\_.' .' \\M\n" +
"                /:  : _/  :/             \\  :\\_:  : \\E\n" +
"               /. `._/ |`./               \\. | \\_. `.\\P\n" +
"              /  :_/  /: /                 \\: \\  \\_  :\\H\n" +
"             / ._/   /' /                   \\ '\\   \\_ .\\\n" +
"            /__/    |  /                     \\  |    \\__\\\n" +
"                    |_/                       \\_|");
        
            
            System.out.println(nome + "O que é issso??????\nAhhhhhhhhhhhhhhhhhh que dor!!!!!!!!!!!!!!");
            
           
            
            
            System.out.println("   ______________________________________________________________________\n" +
"  |:..                                                      ``:::%%%%%%HH|\n" +
"  |%%%:::::..                    ??????????????                `:::::%%%%|\n" +
"  |HH%%%%%:::::....._______________________________________________::::::|\n" +
"\n" +
"            ________   ___   ____\n" +
"           / __   __| / _ \\ |  _ \\\n" +
"     ______> \\ | |   |  _  ||    /_____________________________\n" +
"    / _______/ |_|   |_| |_||_|\\______________________________ \\\n" +
"   / /                                                        \\ \\\n" +
"  | |                                                          | |\n" +
"  | |      A procura do mestre:                                | |\n" +
"  | |                                                          | |\n" +
"  | |                                                          | |\n" +
"  | |      Fase 01: Kariane Coura                              | |\n" +
"  | |      Fase 02: Daniel Kudo                                | |\n" +
"  | |      Fase 03.1: Phellype Guilherme                       | |\n" +
"  | |      Fase 03.2: Pedro Uemura                             | |\n" +
"  | |                                         Continua...      | |\n" +
"   \\ \\____________________________    _   ___   ____   _______/ /\n" +
"    \\___________________________  |  | | / _ \\ |  _ \\ / _______/\n" +
"                                | |/\\| ||  _  ||    / > \\        LS\n" +
"                                 \\_/\\_/ |_| |_||_|\\_\\|__/\n");
     System.out.println(nome+", você descobrirá que muitas das verdades às quais nos prendemos dependem do nosso ponto de vista.");
        System.exit(0);
   }
            static void morre() {
        System.out.println("\nGAME OVER\nQUE A FORÇA ESTEJA COM VOCÊ."
                + "\n\nJogo desenvolvido pelo grupo-05 BSI:"
                + "\nDaniel Kudo"
                + "\nKariane Coura"
                + "\nPedro Uemura"
                + "\nPhellype Guilherme"
                + "\n\nEsperamos que tenha gostado.");
             }
}
