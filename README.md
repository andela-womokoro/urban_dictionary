# UrbanDictionary

[![Build Status](https://travis-ci.org/andela-womokoro/urban_dictionary.svg)](https://travis-ci.org/andela-womokoro/urban_dictionary)

Urban dictionary is a package that stores urban words (slangs) and their meanings in an associative array. It also stores examples of how each urban word is used. The meaning of urban words can be edited, and words can be deleted from the dictionary.

The package also ranks words in a sentence based on the number of occurrence of each word in any given sentence.

## Design
The package contains the following classes
- UrbanWords: contains the array where urban words are stored i.e. the dictionary
- Crud: contains methods to read words from the dictionary, add new words, update the meaning of existing words, and delete words.
- Ranking: contains methods to count the occurrences of words in any given sentence and rank the words based on their occurrence.

## Install
via composer

```
$ composer require wilson/cp1
```

## Usage

- Add urban words to the dictionary

```
$array = ["slang"=>"word", "description"=>"meaning of word", "sample-sentence"=>"example usage"];
Crud::create($array);
```

- Retrieve all words in the dictionary

```
$arr = Crud::getAll();
```

- Retrieve a single word from the dictionary

```
$arr = Crud::find("word");
```

- Update a word, its meaning, or its sample sentence

```
Crud::update("word", "field to update", "new value");
```

- Delete a word

```
Crud::delete("word");
```

- Rank words in a sentence

```
$sampleSentence = "a sample sentence...";
print_r(Ranking::rank($sampleSentence));
```

## Testing

If the  folder containing your test classes is "tests"

```
$ phpunit tests
```

## Change log
Please check out [CHANGELOG](CHANGELOG.md) file for information on what has changed recently.

## Contributing
Please check out [CONTRIBUTING](CONTRIBUTING.md) file for detailed contribution guidelines.

## Security

If you discover any security related issues, please email wilson.omokoro@andela.com instead of using the issue tracker.

## Credits
Urban Dictionary is maintained by Wilson Omokoro.

## License
UrbanDictionary is released under the MIT Licence. See the bundled [LICENSE](LICENSE.md) file for more details.


