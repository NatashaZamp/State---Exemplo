# State---Exemplo
Atividade

public class Exemplo {  
  
    public static void main(String[] args) {  
        try {  
            new Exemplo().executa();  
        } catch (Throwable t) {  
            t.printStackTrace();  
        }  
    }  
  
    private void executa() {  
        Estado estado = Estados.ESTADO_1;  
        System.out.println(estado);  
  
        estado = estado.vaiProEstado2();  
        System.out.println(estado);  
  
        estado = estado.vaiProEstado3();  
        System.out.println(estado);  
  
        estado = estado.vaiProEstado1();  
        System.out.println(estado);  
    }  
}  

-----------------------------------------------------------------------
public class Estados {  
  
    public static final Estado ESTADO_1 = new Estado1();  
    public static final Estado ESTADO_2 = new Estado2();  
    public static final Estado ESTADO_3 = new Estado3();  
}  


public interface Estado {  
  
    Estado vaiProEstado1();  
  
    Estado vaiProEstado2();  
  
    Estado vaiProEstado3();  
}  

------------------------------------------------------------------------------
public class Estado1 implements Estado {  
  
    @Override  
    public Estado vaiProEstado1() {  
        return Estados.ESTADO_1;  
    }  
  
    @Override  
    public Estado vaiProEstado2() {  
        return Estados.ESTADO_2;  
    }  
  
    @Override  
    public Estado vaiProEstado3() {  
        return Estados.ESTADO_3;  
    }  
  
    @Override  
    public String toString() {  
        return "Eu sou o " + getClass().getSimpleName();  
    }  
}  

-----------------------------------------------------------------------------
public class Estado2 implements Estado {  
  
    @Override  
    public Estado vaiProEstado1() {  
        return Estados.ESTADO_1;  
    }  
  
    @Override  
    public Estado vaiProEstado2() {  
        return Estados.ESTADO_2;  
    }  
  
    @Override  
    public Estado vaiProEstado3() {  
        return Estados.ESTADO_3;  
    }  
  
    @Override  
    public String toString() {  
        return "Eu sou o " + getClass().getSimpleName();  
    }  
}  

----------------------------------------------------------------------------
public class Estado3 implements Estado {  
  
    @Override  
    public Estado vaiProEstado1() {  
        return Estados.ESTADO_1;  
    }  
  
    @Override  
    public Estado vaiProEstado2() {  
        return Estados.ESTADO_2;  
    }  
  
    @Override  
    public Estado vaiProEstado3() {  
        return Estados.ESTADO_3;  
    }  
  
    @Override  
    public String toString() {  
        return "Eu sou o " + getClass().getSimpleName();  
    }  
}  
