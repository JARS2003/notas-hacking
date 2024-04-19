## Objetivo
This vault uses ASCII encoding for the password. The source code for this vault is here: [VaultDoor4.java](https://jupiter.challenges.picoctf.org/static/834acd392e0964a41f05790655a994b9/VaultDoor4.java)
## Solución
```
Modifique el codigo:
import java.util.*;

  

class VaultDoor4 {

    public static void main(String args[]) {

    // I made myself dizzy converting all of these numbers into different bases,

    // so I just *know* that this vault will be impenetrable. This will make Dr.

    // Evil like me better than all of the other minions--especially Minion

    // #5620--I just know it!

    //

    //  .:::.   .:::.

    // :::::::.:::::::

    // :::::::::::::::

    // ':::::::::::::'

    //   ':::::::::'

    //     ':::::'

    //       ':'

    // -Minion #7781

        byte[] myBytes = {

            106 , 85  , 53  , 116 , 95  , 52  , 95  , 98  ,

            0x55, 0x6e, 0x43, 0x68, 0x5f, 0x30, 0x66, 0x5f,

            0142, 0131, 0164, 063 , 0163, 0137, 0146, 064 ,

            'a' , '8' , 'c' , 'd' , '8' , 'f' , '7' , 'e' ,

        };

       String password = "";

        for (byte b : myBytes) {

            password += (char)b;

        }

        System.out.println("picoCTF{"+password+"}");

    }

}
picoCTF{jU5t_4_bUnCh_0f_bYt3s_f4a8cd8f7e}
```
## Notas adicionales
## Referencias 