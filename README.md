# Banco
public class Ejercicio_banco {

   
    public static void main(String[] args) {
       
        Scanner entrada = new Scanner(System.in);

        int saldos[] = new int[12];
        int mesmayor=0;

        for (int i = 0; i < 12; i++) {
            System.out.print("Saldo del mes" + (i + 1) + ":");
            saldos[i] = entrada.nextInt();
        }
        
        int negat=0;
        for (int i = 0; i < 12; i++) {
            if (saldos[i] < 0) {
                negat++;
                System.out.println("saldo negativo en el mes" + (i + 1));
            }
        }
        if (negat==0){
            System.out.println("Usuario no tiene deuda");
        }
        
        
        
        int aux=0;
        for (int i =0 ; i<12;i++){
            if (saldos[i]>aux){
                aux = saldos[i];
                mesmayor=i+1;
            }   
        }
        System.out.println("El mes de mayor saldo fue el "+mesmayor);
        
        int suma= 0;
        
        for (int i =0 ; i<12;i++){
            suma = suma + saldos[i];
        }
        int promedio=suma/saldos.length;
        
        System.out.println("promedio mensual es "+promedio);
    }


