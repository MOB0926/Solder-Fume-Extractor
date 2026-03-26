# Solder-Fume-Extractor
   

# Why?

- I made this project because I needed a fan extarctor in general and thought it would be fun to just make one as a project for Blueprint, in my effrot to gain experience in engeneering and design.

# What?

- This project is my attempt at making a custom fume extractor using a 120mm pc fan and a custom PCB.
   
- In order to not waste a full MCU on just a fan I opted to add a few features and make this fan feature a rotary encoder, OLED display, and GPIO pins for working on projects.
        
- The fan and PCB are housed in a custom 3D-Printed case using some pc fan mounting screws
       
- My original goal with the design was to make it a economic as possible, but with the nesscesity of a custom PCB I opted instead to focus my main goal on hand-soldering the PCB, which is something I have been wanting to learn. 
        
# Case
       
- The design began with the case, which i brainstormed untill i developed a general idea in my head.
   
- Once i had a general idea I began taking measurements and designing every piece in Onshape.
   
- I started with the main body, keeping in mind space and acces to the PCB and a way to mount the fan.
    
<img width="850" height="492" alt="image" src="https://github.com/user-attachments/assets/fe2b1caf-e77d-4589-8dca-baa1270dbf36" />
   
- I whent with a panel at the bottom, and slots on the sides which would hold the post that supported the fan.
   
<img width="317" height="649" alt="image" src="https://github.com/user-attachments/assets/a3663d22-c2c8-43c2-b435-c7bb68902e42" />
         
<img width="765" height="375" alt="image" src="https://github.com/user-attachments/assets/e2c82398-e1d0-4050-9ca3-d86176819f33" />
         
- After I was done with the base, I needed a way to mount the fan and add a filter to stop myself from touching the blades.
           
- I decided on a casing that would wrap around the fan and allow me to mount it to the posts, and a custom honey-comb filter
         
<img width="544" height="542" alt="image" src="https://github.com/user-attachments/assets/e8792c44-f1b4-44c2-a7af-6f6b0b5b8c87" />
         
<img width="612" height="622" alt="image" src="https://github.com/user-attachments/assets/65ecd46c-f51c-465a-8eb5-fcccff46a816" />
           
- Finally I inserted all my parts into an assembly where I put everything together
          
<img width="588" height="672" alt="image" src="https://github.com/user-attachments/assets/59e2c646-738d-4f9e-a54b-86ee025d03ea" />
      
# PCB

- I made the case first in order to figure out the dimmensions of the PCB I would be able to include.
   
- My original idea was to use an rp2040 as I have experience with it and a very over complicated adjustable boost converter to power the fan, but it was too much for me and I was unable to verify it would work before finishing the project, so I completely restructured my PCB in a V2
     
- V2: This version is much more simple and includes all hand-solder friendly components in order to acomplish my goal. I opted for an ESP32 module and a basic 5 to 12 volt boost converter.
   
<img width="1147" height="788" alt="image" src="https://github.com/user-attachments/assets/ef1002a8-5b24-48ac-abb1-3501a5748f3a" />
           
<img width="1127" height="460" alt="image" src="https://github.com/user-attachments/assets/ea08d71a-5c57-432b-a244-03f6e7f955ef" />
             
<img width="1003" height="386" alt="image" src="https://github.com/user-attachments/assets/79c2ce92-0add-449e-b6bb-bc18991cf275" />
        
# Firmware
         
- This design does not require any firmare to work because of how the PCB works but you can digitally disable the fan through a mosfet (using IO6 on the MCU). I made google Gemini write me a quick c++ script for it which is placed in the code.txt file
       
- This board can use other languages like CircuitPython using the (ESP32-C3-Lyra V2.0 by Espressif) release as it uses the same MCU so it should work fine. But you can use whatever suits your project.

# Cost

- PCB: $2.10 (plus shipping)
- PCB Components: $19.19 (plus shipping)
- PC Fan: $10-$30 (or free if you have a spare one)
- PC Fan Mounting Screws: $5 (or free if you have a PC with spares)
- 3D-Printing Fillament: (unknown yet)
