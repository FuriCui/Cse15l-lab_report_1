## Find

## 1. -type

`[l3cui@ieng6-202]:skill-demo1-data:292$ find ./written_2/ -type d
./written_2/
./written_2/non-fiction
./written_2/non-fiction/OUP
./written_2/non-fiction/OUP/Abernathy
./written_2/non-fiction/OUP/Berk
./written_2/non-fiction/OUP/Castro
./written_2/non-fiction/OUP/Fletcher
./written_2/non-fiction/OUP/Kauffman
./written_2/non-fiction/OUP/Rybczynski
./written_2/travel_guides
./written_2/travel_guides/berlitz1
./written_2/travel_guides/berlitz2`

Above is the first example, where `-type d` stands for directory type, where find command searches only directory under current directory. This is useful since it can automatically discern from directory or files, which can save us lots of time dealing with similar name of directory and file.

`[l3cui@ieng6-202]:skill-demo1-data:296$ find ./written_2/ -name Beijing-History.txt  -type f
./written_2/travel_guides/berlitz2/Beijing-History.txt`

The command `type f` stands for files type, it is useful when we only want to have files in our output, instead of doing `-name *.txt`.

Site Source:https://www.youtube.com/watch?v=skTiK_6DdqU

## 2. -exec

`[l3cui@ieng6-202]:skill-demo1-data:299$ find ./written_2/ -name Beijing-History.txt  -exec rm {} +
[l3cui@ieng6-202]:skill-demo1-data:300$ find ./written_2/ -name Beijing-History.txt  -type f`

Above, that the `-exec` is a command that is used for us to execute a command against all the items in the results, command `rm` deletes the item, and `{}` puts the result inside, and excute the command. `+` is used to terminate the find command when we use exec option, if not add it, it won't let u run. After explaining all this, we can see that after running the command line, when we want to search the file, it is gone. Thus the rm command executed on the file succesfully.

`[l3cui@ieng6-202]:skill-demo1-data:301$ find ./written_2/ -name Bali-History.txt  -exec grep "Hinduism" {} +
Hinduism Comes to Bali
In the eighth and ninth centuries a.d., several Buddhist rulers in Java converted to Hinduism, along with their subjects. This time, many people in Bali followed suit, perhaps attracted by the complex Hindu mythology — the Balinese today still have a love of the old stories — and by the way their local gods could be housed easily in the crowded Hindu pantheon. Around 930, the kingdom of East Java conquered Bali and the conversion process accelerated. A mild form of the caste system and the concept of the Hindu trinity of Brahma, Shiva, and Vishnu were introduced. But Bali was no mere vassal state of Java. From 1019 to 1042, Airlangga, son of the Balinese king Udayana, ruled over East Java with the help of a Javanese princess, while his young brother acted as regent in Bali. During the 12th and 13th centuries, Bali was often independent.`

Here I used `grep` to the find the string `"Hinduism"` inside the `Bali-History.txt` file after the command `-exec`, where `{}` is the results of the item we find, and is the same reason that works in the last example. 

Site Source:https://www.youtube.com/watch?v=skTiK_6DdqU

## 3. -name

`[l3cui@ieng6-202]:skill-demo1-data:303$ find ./written_2/ -name Bali-History.txt                                
./written_2/travel_guides/berlitz2/Bali-History.txt`

This command option `-name` is used to find the file with the exact string we provide, and as the result it returns the absolute path of the file in the directory.

`[l3cui@ieng6-202]:skill-demo1-data:307$ find ./written_2/ -name Crete-History.txt
./written_2/travel_guides/berlitz2/Crete-History.txt`

Here is also a similar situation when we use -name, we just type the string we want exactly and the output will give us an absolute path of the file location.

Site Source:https://www.youtube.com/watch?v=oPdFGUrq-XQ

## 4. -size/-empty

`[l3cui@ieng6-202]:skill-demo1-data:313$ find ./written_2/ -size +50M `

Above, the command `-size` is used to specify the item's size. Here I wanted to search for a file that is at least 50MB, which returns nothing. This indicate that there exists no files that is up to 50MB which is correct.

`skill-demo1-data:314$ find ./written_2/ -empty`

Here, this command option is obvious. `-empty` option specifies that the file is empty which it returns nothing at the cmd table since there is no empty files in written_2 since they are written. 

Site Source:https://www.youtube.com/watch?v=KCVaNb_zOuw