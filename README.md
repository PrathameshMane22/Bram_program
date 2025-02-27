# Bram_program
This project deals with creating a Block memory in vivado, creation of .coe file (using python / matlab) reading COE file in BRAM, writing testbench and observing simulation

1. By using the COE_creation_python, you can create .coe file data for sine and cosine signal.
   
2. Then in Vivado open the ip catalog and select the "block memory generator" you will be redirceted to the window shown in the image below.
   
![image](https://github.com/user-attachments/assets/c5904fed-9a54-4127-8844-df40157e0ee4)

3. Select the memory type as single port RAM (as for basic use we will be using single port only)
   
4. Then in "other Options" select the .coe file that was created
   
5. Check the summary and click on OK

6. Using the Bram_testbench file that is attached here you can generate the simulation. (But this will generate only single sine wave)

7. Using the Continuous_wave_testbench file that is attached here you can generate the simulation. (This will generate a continuous sin wave)
8. Result of simulation (just for reference)
   
![image](https://github.com/user-attachments/assets/83a92085-9ad8-41a3-8879-cd6aabe5fd26)


For any additional doubts, contact : Prathammane18@gmail.com

