# barcode_faker.R
Update: If you have access to multiple cores, use the faster parallelized version (barcode_faker_parallel.R) by Luis Diaz. You will need to install the doSNOW package.

Here's a brief guide to get you started using the barcode_faker function in R! Many researchers who use TASSEL
don't regularly work with the command line. Don't worry-- you don't need to be an R expert to use this function.
Remember, you only need to process your files with barcode_faker if they are demultiplexed. If your files are
demultiplexed, then each of your individuals is in a different FASTQ file. If your file isn't demultiplexed, then
you have a really big file for each lane of sequencing you did, and you don't need this function. This guide was
written for Windows users- some of the details may be a little different if you are on a Mac.

1. Install R and RStudio if you haven't. (See other online guides.)
2. Open RStudio.
3. There are many ways to import the function, but here are three easy options. You only need to do one of these: pick a, b, or c.
         
         a. 
         1. Go to this link: https://github.com/labroo2/rtassel_supp/blob/master/barcode_faker.R
         2. Copy all the function text, starting from # on line 1 and ending at line 125.
         3. Paste the function text into the Console tab of RStudio. (The Console tab is usually in the
         bottom left of RStudio, and it usually has a blue > starting the first line.)
         4. Hit Enter.
      
      OR

         b. 
         1. Right-click barcode_faker.R on this webpage (above).
         2. Select "Save link as..."
         3. Go to a folder where you want to save the function. For example, you could select your Documents folder.
         4. Click save.
         5. Open File Explorer or Finder. Navigate to the folder where you saved the function, and double-click on
         your barcode_faker.R file. It should open in RStudio. If it doesn't, you can right-click barcode_faker.R
         and click Open With, then click RStudio.
         6. Once the file is opened in RStudio, highlight all of the text, which will be in the top left of RStudio.
         While the text is highlighted, click "Run" in RStudio. It is a small button with a green arrow above
         the text of the function.
      
      OR
      
         c. Use source() on the path to the saved function file, or clone into the repository.
      
      You only need to do one of a, b, or c.
      
4. If you successfully imported the function, then "barcode_faker" will show up in the Environment tab of RStudio
      under the Functions section.
   Another way to check if the function was imported is to type "barcode_faker" (excluding the quotation marks) in
   the Console tab of RStudio, then hit Enter. If the function was imported, then the text of the function will 
   spew into the Console. If the function was not imported, then you will see "Error: object 'barcode_faker' not
   found".
 
 5. Now that you imported the function, you can get ready to run it. First, navigate to your FASTQ files. If they
 are zipped, you must unzip them. So if your files have a .fastq.gz extension, or .fq.gz, you need to unzip them.
 When they are unzipped, they will have just a .fastq or .fq extension. See other online guides for how to unzip.
 
 6. Once your files are unzipped, make a new folder where your output files will go. For example, if your FASTQ files
 are inside your Documents folder inside another folder called myFASTQs, you could make another folder in the Documents
 folder called tasselFASTQs. If your original FASTQs are in more than one folder (for example, lane1, lane2, lane3), then
 you must move them all into the same folder (for example, myFASTQs) to guarantee the function will work.
 
 7. Now, go back to RStudio. Click "Session", then "Set Working Directory", then "Choose Directory". Navigate to the new
 folder where you want your output files to go (tasselFASTQs in our example). Don't skip this step, or it will be hard to
 find your output files later. If you do forget, check the Documents folder first for your output files.
 
 8. This step may be tricky, so try not to get frustrated. Open File Explorer, then navigate to the folder where your
 FASTQs are (myFASTQs in our example). Open the folder. You should see all your FASTQ files inside. Right-click one of
 the FASTQ files (doesn't matter which one), then click "Properties". A box will pop up. Where it says "Location:", you
 will see something like C:\Users\yourname\Documents\myFASTQs . It may be slightly different. But go ahead and copy
 that text after location.
 
 9. Now, go to RStudio. In the Console, type barcode_faker(
 
 10. Paste the location (from Step 9). Now you have something like barcode_faker(C:\Users\yourname\Documents\myFASTQs
 
 11. Change all the backslashes to forward slashes. Now you have something like barcode_faker(C:/Users/yourname/Documents/myFASTQs
 
 12. Then, end the parenthesis. Add quotation marks around the location. You have now have
      barcode_faker("C:/Users/yourname/Documents/myFASTQs")
 
 13. Hit Enter. The program will start running! Your output files should go to the folder you made in Step 6.
     If not, they are in your working directory. The script will print when each of your files is finished. You
     will know the program is done when you see a blue > at the start of the line in the console again.
 
 
 
 
