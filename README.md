# w2v_with_large_text

```python
from gensim.models import Word2Vec
class Sentence_Generator:
	def __init__(self, file_path):
		self.file_path = file_path
	def __iter__(self):
		with open(self.file_path, 'r', encoding='utf-8') as f:
			for line in f:
				yield line.strip().split()

sentences = Sentence_Generator(".../file.txt")
model = Word2Vec(sentence)

# file.txt
# file.txt must contain one sentence per line.
# And each word must be separated by white space.
# example is as below:
# this is an example sentence
# I want to train w2v with large text file
```
