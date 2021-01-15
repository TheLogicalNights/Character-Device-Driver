Include header files 
Create user defined macros 
add meta data 
declare the functions 
initialise file_operations structure 
define init method 
    register device register_chardev 
    create class create_class 
    create device device_create 
define exit or cleanup method 
    unregister device 
    destroy the class 
    destory the device 
define dev_open 
    increment the refercene count 
define dev_release 
defien dev_read 
    read the data 
defien dev_write 
    write the data 

--------------------------------------- 

Build the driver using makefile 
Create the application as a client for the driver which will open /dev/Marvellous_Driver_1 file 
write into that file 
read the data from that file 
close that file 
Build the executable pf client application 
insmod the driver 
run the client application 
check the logfile for the message
unload the driver using rmmod

    char_init               char_exit
1)  register_chardev        1)device_destroy        
2)  class_create            2)class_destroy
3)  device_create           3)unregister_chrdev