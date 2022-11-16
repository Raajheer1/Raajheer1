```python
from life.species import Human
from skills import python, javascript, go, c++, html, css, other
from datetime import date
from random import choices
from os import getenv


class RaajPatel(Human):
    def __init__(self, username='raajheer1'):
        self.name = f'Raaj {0} Patel'.format(choices([os.getenv('MIDDLE_NAME'), 'T', '']))
        self.pronouns = ['he' and 'him'],
        self.description = '''
            An Electrical Engineering B.S. Student at Texas A&M University. Currently working as a 
            contract software engineer at Presentation Management Systems. 
        '''
        self.aliases = ['Xevion', 'Xevioni']
        self.aliases.extend(map(lambda alias: alias.lower(), (alias for alias in self.aliases)))
        self.skills = {
            'python': [
                python.BeautifulSoup, python.scikit-learn, python.TensorFlow
            ],
            'javascript': [
                javascript.NodeJS, javascript.VueJS
            ],
            'go': [
                go.Gin, go.Gorm
            ],
            'c++': [],
            'html&css': [
                html.Bootstrap4, css.SCSS, css.CSS
            ],
            'other': [
                other.DevOps
            ]
        }
        self.endpoints = {
            'Discord': {'username': 'Raaj Patel', 'discriminator': 7762},
            'Email': {'username': 'the', 'domain': 'raajpatel.dev'}
        }
        self.hobbies = [
            'Programming', 'Aviation', 'Semiconductors', 'Cryptography'
        ]
```
