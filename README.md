# UrbanDictionary
Urban dictionary is a package that stores urban words (slangs) and their meanings in an associative array. It also stores examples of how each urban word is used. The meaning of urban words can be edited, and words can be deleted from the dictionary.

The package also ranks words in a sentence based on the number of occurrence of each word in any given sentence.

# Design
The package contains the following classes
- UrbanWords: contains the array where urban words are stored i.e. the dictionary
- Crud: contains methods to read words from the dictionary, add new words, update the meaning of existing words, and delete words.
- Ranking: contains methods to count the occurrences of words in any given sentence and rank the words based on their occurrence.

# Install
via composer

```$ composer require wilson/urbandictionary```

Then 

```$ composer install```

# Usage

- Add urban words to the dictionary

```$array = ["slang"=>"word", "description"=>"meaning of word", "sample-sentence"=>"example usage"];
Crud::create($array);```

- Retrieve all words in the dictionary

```$arr = Crud::read();```

- Update the meaning of a word

```Crud::update("word", "new meaning...");```

- Delete a word

```Crud::delete($index);```

- Rank words in a sentence

```$sampleSentence = "a sample sentence...";
  print_r(Ranking::rank($sampleSentence));```
  
  
  # Testing
  
  For testing
  
  ```$ phpunit tests```

