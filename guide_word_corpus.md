### The word corpus

I believe by this time varnam is up and running on your computer. You must be able to type in words and see them getting transliterated. Varnam learns as you type, but it can take some serious time before varnam can learn all of your frequently used words.

Have no fear, the word corpus is here. The word corpus is simply a long (really long) list of words that can be downloaded from the internet. Our next task is to download a word corpus and feed it to varnam so that the next time you type a very-complicated word, its already in the suggestions.

#### Download the word corpus

You can download the Hindi and Malayalam word corpus from the [savannah](http://download.savannah.gnu.org/releases/varnamproject/words/) page. The downloaded file is a tarball and you have to extract it. A tarball is like a zip file or a rar file, and is used often in linux. Extract them to a folder.

#### Learn!
To make varnam learn from the word corpus, type the following command in the terminal :

`varnamc -s <lang_code> --learn-from <path_to_folder>`

If I've extracted the malayalam word corpus to my home folder, I would use :

`varnamc -s ml --learn-from /home/kevin/words`

That would result in varnam learning all the words in all the text files contained in the words/ folder. You can ask varnam to learn the contents of individual files by specifying the name of the file instead of the containing folder :

`varnamc -s ml --learn-from words/01.txt`

Try using varnam again and you should see better suggestions. If not, try restarting ibus-daemon (right click on the icon on the panel -> restart) and try again.

######[Next](link)
######[Prev](guide_input_tools.md)