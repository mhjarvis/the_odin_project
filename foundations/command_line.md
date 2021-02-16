### Basic Commands http://conqueringthecommandline.com/book/basics
##### Present Working Directory
    pwd                                 //show current directory
    pwd -P                              //show actual physical path
##### List Files and Directories
    ls                                  //list files
    ls -a                               //include hidden files
    ls -l                               //long form (detailed)
    ls -h                               //human readable
    ls -S                               //sort by size
    ls -t                               //sort by last modified
    ls -r                               //reverse sort
##### Links
Links create associations from one file/dir to another (or 'point' one file or dir to another).

    ln a.txt b.txt                      //source file => linked file
    ln -f a.txt b.txt                   //if file already exists, this will force it
    ln -s a.txt b.txt                   //create a symbolic link to a directory (works with directories and linking to other file systems)
##### Change Directories
    cd ~/Documents                      //use the path you want to nav to
    cd ..                               //navigate up a directory
    cd                                  //navigate to your home directory
##### Creating Directories
    mkdir foo                           //create directory foo
    mkdir -p a/b/c                      //create nested directories
    mkdir -v a                          //verbose mode (-v); will print results of mkdir to console
##### Copying Files
    cp a.txt b.txt                      //source file you want to copy => new file
    cp a.txt b.txt foo                  //copy multiple files (a and b) to directory foo (file file file => directory name)
    cp *.txt foo                        //""
    cp -v a.txt b.txt                   //verbose output
    cp -Rv foo bar                      //recursivly copy directory foo to bar
    cp -f a.txt b.txt                   //use -f to overwrite (forced)
    cp -i a.txt b.txt                   //prompt before overwritting
##### Deleting Files
    rm -v a.txt                         //delete a.
    rm -r test                          //remove directory 'test'
##### Moving Files                      
    mv -v a.txt b.txt
##### Redirecting Output
    ls -a ~ | grep _                    //pipe output of ls to the input of the grep command (find all files in dir containing '_')
    ls -a ~ | grep _ > u.txt            //redirect output and write to file
    < b.txt                             //read from file
    
    
    
    
    
    
    
    
