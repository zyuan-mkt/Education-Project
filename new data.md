## 2019 and 2020 crowdfunding essays
![Number](./figures2/num.png)

### category
'Arts': 'Art Supplies', 'Musical Instruments'

'Supplies': 'Supplies','Books', 'Lab Equipment','Classroom Basics', 'Awaiting Classification','Reading Nooks, Desks & Storage','Flexible Seating','Food, Clothing & Hygiene','Other'

'Tech': 'Technology','Computers & Tablets','Instructional Technology'

'Entertainment': 'Sports & Exercise Equipment','Educational Kits & Games'

'Visits': 'Virtual Trips','Virtual Visitors'

![2019](./figures2/cat_mon19.png)
![2020](./figures2/cat_mon20.png)

### subject_category
'Science': 'Applied Sciences','Environmental Science','Mathematics','Health & Life Science'

'Language': 'Financial Literacy','Literacy','Literature & Writing','Foreign Languages','ESL'

'Social Sciences': 'History & Geography','Social Sciences', 'Economics', 'Civics & Government'

'Health and Sports': 'Health & Wellness', 'Nutrition Education','Special Needs','Gym & Fitness','Team Sports'

'Arts': 'Visual Arts','Music','Performing Arts'

'Extracurricular': 'Parent Involvement', 'Extracurricular','Community Service','Warmth, Care & Hunger','Character Education','Early Development','College & Career Prep','Social Emotional Learning','Other'

![2019](./figures2/sub_mon19.png)
![2020](./figures2/sub_mon20.png)


### grade_level
"Grades PreK-2","Grades 3-5","Grades 6-8","Grades 9-12"

![2019](./figures2/grd_mon19.png)
![2020](./figures2/grd_mon20.png)


### Subject and Category
![SUBJECT](./figures2/yr_mon.png)

![SUBJECT](./figures2/sub.png)
![SUBJECT](./figures2/sub_yr.png)
![SUBJECT](./figures2/yr_sub2.png)
![SUBJECT](./figures2/yr_mon_sub.png)

![CATEGORY](./figures2/cat.png)
![CATEGORY](./figures2/cat_yr.png)
![CATEGORY](./figures2/yr_cat2.png)
![CATEGORY](./figures2/yr_mon_cat.png)

## Structured
`lp ~ 1 + school_state + C(year) + C(month)`

lp - log price

![Regression 1](./figures2/reg1.png)

`lp ~ 1 + CATEGORY + SUBJECT + grade_level + school_percentage_free_and_reduced_price_lunch_eligible + C(year) + C(month)`

![Regression 2](./figures2/reg2.png)

`lp ~ 1 + pca1 + pca2 + pca3 + pca4 + pca5 + pca6 + neg + pos`

where PCAs are first six components of the extracted textfeatures; neg and pos are proportion of positive and negative words

![Regression 3](./figures2/reg3.png)

`lp ~ 1 + CATEGORY + SUBJECT + grade_level + school_percentage_free_and_reduced_price_lunch_eligible + n_words + n_polite + ari + sent_vader + C(year) + C(month)`
n_polite - number of polite words

ari - Automated Readability Index (ARI)

sent_vader - vader sentiment

![Regression 4](./figures2/reg4.png)

`label ~ 1 + CATEGORY + SUBJECT + grade_level + n_words + n_polite + ari + sent_vader`

label - 1 (high poverty), 0 (low poverty)

![Regression 3](./figures2/reg5.png)

`label ~ 1 + pca1 + pca2 + pca3 + pca4 + pca5 + pca6 + neg + pos`

![Regression 4](./figures2/reg6.png)

## Unstructured
### Poverty Level
`Test Loss: 0.508 | Test Acc: 75.02%`

**Rich**

['school\u200b', 'flipgrid', 'sharpers', 'windowless', 'slinkies', '2020/2021', 'playdoh', 'gineers', 'headset', 'duct', 'that-', '-on', 'eight-', 'year-', 'squishies', 'reteaching', '\u200band', 'splitter', 'la', 'para', 'gon', 'mindedness', 'alouds', 'throwable', 'zippered', 'crate', 'engross', 'porch', 'on\u200b', 'departmentalized', 'clicks', 'scanned', 'students-', 'robotic', 'algebraic', 'bead', 'pincer', 'pains', 'chord', 'freshman', 'configured', 'boundless', 'folder', 'audiobooks', 'pouch', 'bookshelf', 'w', 'lockers', 'starter', 'thermochemistry', 'rectangular', 'powers', 'weekday', 'violin', 'seating', 'divider', 'dimensional', 'court', 'covid-19', 'coat', 'browsing', 'adapter', 'progressions', 'infinite', 'chargers', 'cartridge', 'rechargeable', 'awe', 'twelfth', 'percentile', 'flight', 'potting', 'upload', 'i3', 'surf', 'simulators', 'covid', 'vessel', 'is\u200b', 'refills', '=', 'quests', 'twistable', 'debug', 'fantasy', 'energize', 'paddles', '8th', 'drone', 'fluorescent', 'scanning', 'corona', 'bookcases', 'sequel', 'clarinets', 'ebooks', 'repetitive', 'align', 'division', 'kinders']

**Poor**

['individualities', 'benefits', 'textured', 'epidemic', 'kidney', '1000x', 'prevention', 'neighborhoods', 'incomes', 'surveyed', 'disability', 'supplemental', 'soar', 'average', 'urban', 'severe', 'rate', 'chip', 'migrant', 'breakfast', 'market', 'poorest', 'worst', '10-year', 'rising', 'low', 'adoptions', 'demographic', 'cash', 'poor', 'populations', 'rural', 'reap', '2nd-5th', 'illiterate', 'unproductive', 'inequality', 'decrease', 'impoverished', 'living', 'fourths', 'pandemic', 'families', 'possible-', 'affluent', 'net', 'heating', 'welfare', 'fund', 'households', 'laminator', 'bilingualism', 'kinesthetically', 'dollars', 'booming', 'percent', 'existent', 'disadvantaged', '1.9', 'electricity', 'socioeconomic', 'hotels', 'expenses', 'osmos', 'suffering', 'allotment', 'harvest', '%', 'burden', 'iready', 'tuition', 'underprivileged', 'deficit', 'disease', 'monsoon', 'borrowing', 'hyperactivity', 'someday\u200b', '65', 'productivity', 'savings', 'learnings', '1.5', 'consumption', 'cereal', 'chocolate', 'low‑income', 'outbreak', 'boroughs', 'exceeding', 'poverty', 'alleviate', 'cheese', 'income', 'burdened', '$', 'village', 'nt', 'employment', 'million']


### Covid19

`Test Loss: 0.547 | Test Acc: 75.88%`

__2019__

['powerpoints', '200-hour', 'kinesthetically', 'protractors', 'that-', 'qr', 'income\u200b', 'keychains', 'chord', 'harmonies', 'manifold', 'overlapping', 'alouds', 'metallophones', 'modal', 'playdough', 'aquarium', 'world\u200b', 'scavenger', 'repertoire', 'orbit', 'multimodal', 'touchscreen', 'students-', 'hyperdocs', 'working\u200b', 'rectangular', 'bookcase', 'smartboard', 'weave', 'movable', 'lifecycle', 'progressions', '504s', 'decimal', 'temperature', 'classroom-', 'boo', 'stringed', '1000x', 'inclusiveness', 'seating', 'selfie', 'curved', 'auditorium', 'hunts', 'cohesive', 'slime', 'configured', 'zipper', 'melodies', 'on\u200b', 'zippered', 'florescent', 'thematic', '3d', 'fist', 'hands-', '\u200band', 'teaser', 'wasn', 'iready', 'coughing', 'makerspace', 'hoop', 'sneakers', 'rays', 'efficacy', 'fictional', 'saucer', 'modular', 'freshly', 'blacktop', 'laminate', 'counters', 'pale', 'weighted', 'nonfiction', 'writings', 'interface', 'courtyard', 'cage', 'downloaded', 'customizable', 'extracurricular', 'sunglasses', 'philosophy', 'sketches', 'nationalities', 'circular', 'confines', 'loveable', 'poems', 'purifier', 'foldable', 'ensembles', 'productively', 'percentile', 'bracelets', 'assemblies']

__2020__

['wealth', 'preforming', 'metro', 'dose', 'rates', 'productivity', 'region', 'affected', 'breakfast', 'lodging', 'deficit', '85', 'dollar', 'exposure', 'camps', 'beacon', 'village', 'plentiful', 'households', 'homelessness', 'sustenance', 'weak', '6-', 'counties', '49', 'burden', 'rate', 'handouts', 'seizures', 'spread', 'stricken', 'reduction', 'lexia', 'reminder', 'instability', 'loan', 'racially', 'hardships', 'qualifies', 'pizza', 'alleviate', 'flood', 'infectious', 'blankets', 'rural', 'lagging', 'endured', 'shortage', 'low', 'refugee', 'survivors', 'upkeep', 'expend', 'socio', 'tuition', 'reliant', 'reunite', '®', 'prices', 'stigma', 'chronic', 'percent', 'diminish', 'urban', 'life\u200b', 'city\u200b', 'injustices', 'estimate', 'inequality', 'faraway', '%', 'socioeconomic', 'freezing', 'fears', 'exceptionalities', 'disadvantaged', '$', 'pandemic', 'influx', 'rising', 'exceed', 'low‑income', 'day\u200b', 'illiteracy', 'expenses', 'income', 'rains', 'flooding', 'poorest', 'impoverished', 'eight-', 'poverty', 'slinkies', 'pollution', 'possible-', 'playdoh', 'gineers', 'commute', 'candling', 'burdened']


When delete "covid","covid19","covid-19","Covid","COVID","Covid-19","COVID19","COVID-19"

`Test Loss: 0.700 | Test Acc: 50.69%`

**2019**

['\u200band', 'slabbed', 'all-', 'need\u200b', 'grateful-', 'index', 'selfie', '\u200b', 'screencast', 'grade\u200b', 'dabbers', 'classdojo', 'throwable', 'kidshardworking', 'aloud\u200b', 'wonderings', 'de', 'ally', 'departmentalize', 'elearn', 'peacefully', 'notetaking', 'v', 'godsend', 'nationalities', 'bellies', 'degrees', 'bedroom', 'container', 'drug', 'futures', 'bees', 'diapers', 'clicking', 'intentional', 'motors', 'tac', 'grips', 'armrest', 'unplug', 'powerpoints', '-the', 'waving', 'endurance', 'fixing', '°', 'intonation', 'punch', 'pot', 'measures', 'exponentially', 'properties', 'eraser', 'hurdle', 'streaming', 'stake', 'exceptionalities', 'wasting', 'cozier', 'giant', 'fought', 'zest', 'approval', 'cups', 'waking', 'encompasses', 'absorption', 'misplaced', 'stressors', 'delicious', 'mighty', 'chewing', 'plastics', 'printables', 'transport', 'reliant', 'teachable', 'drastic', 'marine', 'removed', 'below', 'stakes', 'combat', 'stitching', 'hep', 'browse', 'flora', 'worms', 'hole', 'sweeper', 'intense', 'conjunctions', 'understandings', 'bay', 'donorschoose.org', 'seamlessly', 'goggle', 'lap', 'sweaty', 'hasn']

**2020**

['program-', 'bookcase', 'suitable', 'frustrate', 'turtle', 'rockets', 'brightly', 'equivalency', 'forests', 'baccalaureate', 'nearest', 'reteaching', 'twistable', 'betterment', 'graciously', 'heritages', 'frogs', 'depression', 'advertisements', 'decline', 'fragments', 'trees', 'helper', 'bear', 'highlighted', 'refreshed', 'earthquake', 'centrifuge', 'forest', 'furthering', '..', 'habitats', 'progresses', 'sheltering', 'smell', 'reclassified', 'unreal', 'sketchbooks', 'minis', 'bin', 'bowl', 'experimental', 'proximity', 'diversify', 'dinosaur', 'synchronously', 'pillars', 'castle', 'facilitators', 'wealthier', 'cars', 'expedition', 'advertising', 'littlest', 'curate', 'conjecture', 'asap', 'streams', 'emotional\u200b', 'insatiable', 'firsties', 'procedures', 'lamination', 'replenishes', 'spruce', 'spirits', 'graphs', 'viruses', 'communal', 'religions', 'brick', 'lake', 'relations', '27th', 'ancestry', 'steadfast', 'low-', 'masters', 'certified', 'gardens', 'to\u200b', 'impairment', 'console', 'trails', '12:1:1', 'ranching', 'marjority', 'income\u200b', 'iseeme', 'free\u200b', 'hokki', 'giftedness', 'unifix', 'kinesthetically', 'manuscript', 'pre-', 'kinders', 'bandaids', 'life\u200b', 'hands-']

### Subsample Data - Category

**Entertainment (ent)**

`Test Loss: 0.569 | Test Acc: 72.49%`

**Rich**

['equivalency', 'commodities', '3rd', 'compliment', 'scripts', 'scribe', 'jigsaw', 'cubby', 'slap', 'thrives', 'asks', '2nd', 'tray', 'launcher', 'graphics', 'integrates', 'raining', 'string', 'adventure', 'beginner', '8th', 'sequencing', 'delivery', 'dominoes', 'cube', 'computational', 'imitation', 'expressively', 'wouldn', 'programmable', 'bookshelf', 'square', 'editing', 'fabric', '5th', 'winner', 'swivel', 'graphs', 'chunks', 'programmer', 'connectors', 'authentically', 'drawstring', 'investigative', 'ah', 'epic', 'analog', 'fits', 'tile', 'three‑quarters', 'symbolic', 'classical', 'bundles', 'reads', '7th', '6th', 'figurative', 'sequence', '4th', 'threw', 'scented', 'smartphone', '\u200band', 'washable', 'poems', 'weighted', 'storybook', 'gel', 'activating', 'bracelets', 'conductivity', 'canopy', 'reteach', 'personalize', 'compound', 'playdough', 'vests', 'cvc', 'students\u200b', 'sectional', 'kindergarten-5th', 'lemonade', 'knit', 'algebra', 'whiteboard', 'cereal', 'orally', 'inventor', 'chromebooks', 'receptively', 'script', 'lightweight', '-19', 'nook', 'students-', 'pinnies', 'ozobots', 'smartboard', 'alouds', '®']

**Poor**

['incomes', 'are\u200b', 'deficits', 'on\u200b', '3-', '2019/2020', 'kickballs', 'income', 'geoboard', 'uninterrupted', 'productivity', 'poverty', '%', 'northeast', 'makerspace', 'kinders', 'percentage', '123s', 'revenue', '2nd-5th', 'hourly', 'sanitation', 'lending', 'poorest', 'hunts', 'neediest', 'dependent', 'degrees', 'tissue', 'equality', 'cubelets', 'farming', 'accommodations', '$', 'township', 'outbreak', 'rate', 'refugee', 'rates', 'equity', 'honoring', '225', 'educates', 'perks', 'muscular', 'enrollment', 'underfunded', '..', 'disadvantaged', 'losses', 'socioeconomic', 'supporters', 'archaeologists', '90', 'low', 'population', 'households', 'percent', 'impoverished', 'castle', 'racial', 'erosion', '=', 'diagnosed', 'depleted', 'ons', 'palsy', 'hugged', 'elephant', 'explorative', 'cuties', 'spinner', 'camps', '86', '45', 'benefits', 'aids', 'lowincome', '12:1:1', 'families', 'uplift', 'hurricanes', '7-year', 'sparked', 'neighboring', 'kindergartens', 'rover', 'storms', 'steady', 'fund', 'withdrawals', 'dino', 'contributes', 'undergone', 'olds\u200b', 'bin', 'dry', 'continual', 'scavenger', 'dose']


**Tech (tech)**

`Test Loss: 0.499 | Test Acc: 76.58%`

**Rich**

['hardwiring', 'wonderings', 'musix', 'reusable', 'exceptionalities', 'important\u200b', 'screencast', 'convergent', 'dice', 'tangrams', 'reteaching', 'flipgrid', 'dialects', 'moveable', 'laminator', 'recorder', 'formatting', 'highlighters', 'ozobot', 'disseminated', 'abstract', 'asynchronous', 'unity', 'donorschoose.org', 'acrylic', 'percentile', 'genres', 'blank', 'starfall', 'videography', 'covid', 'decimals', 'synchronous', 'selphy', 'cookie', '-5th', 'smartboard', 'neon', 'five-', 'bluetooth', 'aligns', 'modalities', 'showcasing', 'protocols', 'wouldn', 'mics', 'algebra', 'subsystems', '-we', 'reset', 'makey', 'syllable', '.and', 'textures', 'seed', 'decodable', 'amplifier', 'ukulele', 'biomes', '9th-12th', 'docking', 'discrete', 'phonics', 'outs', 'diagram', 'gold', 'reflex', '2018', 'carries', 'console', 'motion', 'laser', 'rock', 'graph', 'grammatical', 'instills', 'divergent', 'arm', 'sharpener', 'inventions', 'formats', 'eventual', 'bells', 'sized', 'chord', 'laminating', 'twentieth', 'peaceful', 'playlists', 'visions', 'webquests', 'paced', 'unison', 'beginner', 'rendering', '1:1', '90th', 'whiteboard', 'lens', 'trial']

**Poor**

['populations', 'dependent', 'encountered', 'vulnerable', 'sore', 'survey', 'cups', 'ozobots', 'unnecessary', 'remainder', 'visited', 'percentage', 'reopen', 'depths', 'rates', 'monthly', '2020', 'price', 'housing', 'fears', 'touchpad', 'inquiries', 'drops', 'mild', 'promotion', 'projected', 'region', 'torn', '75', 'student-', 'classdojo', 'amidst', 'tons', 'suffered', 'uncomfortable', 'economic', 'portability', 'poor', 'homeless', 'mile', 'regroup', 'socialize', 'attainment', 'decrease', 'lower', 'burden', 'coronavirus', 'contagious', 'farming', 'threat', 'rural', 'fallen', 'restaurant', 'socioeconomic', 'north', 'households', 'low', 'wildlife', 'pockets', 'property', 'deficits', 'subsidized', 'rampant', 'incomes', 'insufficient', 'salary', 'infection', 'businesses', 'minimum', 'coats', 'sleeve', 'tuition', 'selfie', 'expenses', 'risen', 'firsties', 'lowest', 'average', 'dramatically', '84', 'pandemic', 'poverty', 'poorest', 'disadvantaged', '%', 'net', 'scarcity', 'quarantine', 'smoother', 'wealthier', 'refugees', 'income', 'nt', 'impoverished', 'neurotypical', 'ticket', 'underserved', '1.5', 'earnings', 'reteach']

**Supplies (sup)**

`Test Loss: 0.516 | Test Acc: 74.87%`

**Rich**

['2020/2021', 'working\u200b', '-and', 'well-', 'wonderings', 'four-', 'departmentalized', 'students-', '3-', 'programable', 'interdisciplinary', 'alouds', 'on\u200b', 'fundations', 'fluently', 'learning-', 'reteaching', 'interconnected', 'rigid', 'playdough', 'toe', 'tummies', 'them\u200b', 'empathetic', 'diagrams', 'toolkit', 'book-', 'graphs', 'mystery', 'dazzling', 'revising', 'viewers', 'teachable', 'ecomonic', 'laminate', 'dystopian', 'beginner', 'revise', 'lamination', 'external', '6th-8th', 'framework', 'pom', 'bonus', 'appreciative', 'mechanism', 'watercolor', 'littles', 'achievable', 'tone', 'quest', 'renovated', 'cursive', 'mature', 'afterschool', 'natures', 'drawers', 'sciences', 'sincere', 'seamlessly', 'removable', 'quizzes', 'captivating', 'seating', 'dolls', 'internship', 'expo', 'drawer', 'pictorial', 'enjoyable', 'changer', 'cherish', 'beautify', 'facilitator', 'deepen', 'illustrator', 'venture', 'journaling', 'constructive', 'geometric', 'strengthens', 'redesign', 'alphabet', 'rows', 'aide', 'adaptable', 'graph', 'curved', 'goofy', 'philosophy', 'redecorate', 'multiplication', 'joins', 'document', 'yay', 'disengaged', 'researched', 'bookshelf', 'cohesive', 'storytelling']

**Poor**

['soaking', 'rising', 'urban', '63', 'capital', 'profit', 'county', 'crops', 'reaches', 'price', 'tops', 'stakes', 'southeastern', 'lunch', 'erasable', 'lake', 'heavy', 'fallen', 'merchant', 'byes', 'groceries', 'temperature', 'syndrome', 'ton', 'rural', 'trapped', 'economic', 'grade\u200b', 'virus', 'vegetables', 'funds', 'foods', 'rescue', 'low', '94', 'mile', 'slid', 'waste', 'socioeconomic', 'achievers', 'diseases', 'male', 'kinders', 'aids', 'b', 'suburbs', 'bandits', 'alleviate', '..', 'aren', 'socio', 'percent', 'isolation', 'ranching', 'neglect', 'meat', 'fell', 'adjusted', 'homelessness', 'percentage', 'discount', 'uncomfortably', 'beds', 'wouldn', 'pollution', 'harsh', 'lion', 'lower', '1/3', 'cord', 'populations', 'underprivileged', 'wealth', 'corona', 'makerspace', 'suffering', 'quarantined', 'symptoms', 'accumulated', '%', '2/3', 'unproductive', 'crumbling', 'violent', 'insecurity', 'rainy', 'foothills', 'self-', 'epidemic', 'income\u200b', 'desert', 'income', 'poverty', 'paycheck', 'cohort', 'day\u200b', 'incomes', 'incidence', 'deficit', 'notetaking']


**Visits (vis)**

`Test Loss: 0.313 | Test Acc: 86.46%`

**Rich**

['gineers', 'students-', '\u200b', '\u200band', 'unifix', 'arsenal', '®', 'olds\u200b', 'bulb', 'that-', 'hyperactivity', 'curve', 'amazes', 'unstructured', '5-', 'division', 'kinders', 'augmentative', 'goggles', 'generational', 've', 'chromebooks', 'electives', 'nook', 'rotated', 'pipe', 'putty', 'proprioceptive', 'curricular', 'multiplication', 'stimulation', 'r', 'mechanical', 'cohesive', 'civilizations', 'tennis', 'matches', 'dirt', 'anti', 'assists', 'blast', 'holes', 'suburb', 'questioning', 'tac', 'flower', 'oh', 'folds', 'percentile', 'spheres', 'collections', 'glitter', 'amazement', 'bustling', 'slides', 'docs', 'cardio', 'rejoin', 'scaffold', 'cvc', 'fluorescent', 'recesses', 'comfy', 'cubes', 'homey', 'stressful', 'endings', 'volcano', 'tub', 'zest', 'her', '1:1', 'crash', 'littles', 'intriguing', 'decimal', 'dinosaur', 'appreciative', 'bubbles', 'cones', 'indoor', 'goodies', 'geometry', 'explosion', 'uncertainties', 'ethnically', 'brick', 'fridge', 'de', 'disorders', 'triumphant', '-', 'unpack', 'boundless', 'rug', 'magnifying', 'algebra', 'adaptable', 'smell', 'pretty']

**Poor**

['2021', 'disabled', 'sandwiches', 'attempt', 'tangram', 'restrictive', 'windows', 'incentives', 'forest', 'female', 'county', 'contains', 'articles', 'documents', 'qualify', 'quarantine', 'immensely', 'labels', 'accommodations', 'languages', 'coincide', 'tablets', 'certified', 'member', 'majority', 'don', 'poor', 'clicking', 'guidelines', 'president', 'curriculums', 'widely', 'permission', 'writers', 'noodles', 'certificate', 'inventors', 'negative', 'creators', '700', 'python', '+', 'washed', 'lifted', '2.0', 'significantly', 'containers', 'link', 'familiarize', 'nt', 'strengthens', 'economically', 'citizen', 'supplied', 'entice', 'virus', 'socio', 'educator', 'passages', 'thriving', 'framework', 'caddies', 'guarantee', 'population', 'households', 'refugees', 'alleviate', 'lightweight', 'apartments', 'coordinate', 'specials', 'geoboard', 'authors', 'ignite', 'canceled', 'prime', 'storybook', 'meals', 'retell', 'global', 'mainstream', 'ticket', 'income', 'decorate', 'rekenreks', 'uppercase', 'credit', '%', 'rocket', 'commute', 'coronavirus', 'pandemic', 'priced', 'folder', 'magnatiles', 'hyperdocs', 'playdough', 'lowercase', 'alouds', 'covid']

**Arts(art)**

`Test Loss: 0.652 | Test Acc: 62.11%`

**Rich**

['grade\u200b', '\u200band', 'ukes', 'kinders', 'alouds', 'rhyming', 'tubano', 'toss', 'cardstock', '6th-8th', 'wildest', 'tray', 'laminate', 'melodic', 'neon', 'multiplication', 'laminated', 'rhythmic', 'brightness', 'electives', 'pitched', 'retell', 'hellos', 'pops', 'melodies', 'fluency', 'crochet', 'ignites', 'framework', 'pop', 'chords', 'innate', 'measurement', 'muscles', 'seating', 'desk', 'prize', 'tenor', 'mystery', 'cozy', 'pinch', 'hammer', 'projected', 'zest', 'packet', 'technologies', 'maze', 'fiction', 'sensing', 'chord', 'boogie', 'storytelling', 'awards', 'knit', 'structural', 'smell', 'ratios', '2019', 'towers', 'adhesive', 'knitted', 'roles', 'workshop', 'scissor', 'progressions', 'stems', 'playdough', 'surfaces', 'electrical', 'hallway', 'hair', 'geometric', 'signage', 'ribbons', '@', 'rugs', 'triangles', 'anchor', 'baritone', 'woodwind', 'circuits', 'focuses', 'guitar', 'festivals', 'mahogany', 'cheering', 'invested', 'compositions', 'percussion', 'phonics', 'dice', 'neat', 'personalizing', 'pots', 'acoustic', 'gaining', 'workforce', 'neighborhoods', 'juices', 'template']

**Poor**

['45', 'aged', 'bundle', 'failure', 'attending', 'devices', 'hygiene', 'falls', 'hate', 'doodle', 'connects', 'evaluated', 'disadvantaged', 'base', '56', 'endure', 'financially', 'percent', 'germs', 'newspaper', 'waiting', 'coronavirus', 'division', '49', 'drive', 'feathers', 'poms', 'degree', 'donated', '3,000', 'c', 'tubas', 'seats', 'reducing', 'motivator', 'federal', 'held', 'guns', 'isolated', '19', 'throwable', 'periods', 'shells', 'hardships', 'arrived', 'households', 'rulers', 'heal', 'fundraiser', '32', 'closed', 'surprised', 'described', 'maintenance', '8', 'reported', 'donors', 'actively', 'received', 'quarantine', 'violins', 'party', 'suffering', 'hit', 'rate', 'homes', 'mold', 'poverty', 'jars', 'incoming', 'adjustable', 'helped', 'skin', 'restraints', 'firsties', 'belongings', 'excessive', 'income', 'apartments', 'pandemic', 'shelters', 'cancer', 'diagnosis', 'severely', 'virus', 'birds', 'corona', '%', 'makerspace', 'dwindling', 'intellectually', '..', 'session', 'hospitals', 'metallophones', 'patients', 'books-', 'price\u200b', '6th-12th', 'brayers']

### Subsample Data - Subject

**Language (lan)**

`Test Loss: 0.492 | Test Acc: 76.97%`

**Rich**

['2020/2021', 'throwable', 'grade\u200b', 'vowel', 'foam', 'canvas', 'cricut', 'rockstar', '5-', 'strings', 'book-', 'x', 'rockstars', 'hop', 'hip', '3-ring', 'choral', 'excites', 'cease', 'ergo', 'plush', 'phonetic', 'dimension', 'themed', 'pure', 'pink', 'syndrome', 'combine', 'curated', 'chromebooks', 'firsties', 'impactful', 'occasions', 'superstars', 'selections', 'smelly', 'repertoire', 'hobby', 'charming', 'portrayed', 'crafting', 'year\u200b', 'transcends', 'digitally', 'greenhouse', 'triangular', 'holder', 'seesaw', 'hatching', 'finishers', 'interdependent', 'appetite', 'cursive', 'depicting', 'geometry', 'gold', 'auditory', 'references', 'tedious', '\u200b', 'parting', 'phonological', 'poem', 'mature', 'formative', 'unfortunate', 'vibe', 'nations', 'arsenal', 'nonfiction', 'littlest', 'y', 'puppet', 'dinosaurs', 'docs', 'teenage', 'genres', 'branching', 'effects', 'actors', '17th', 'translated', 'ingredients', 'fruits', 'dominoes', 'stereo', 'buzz', 'technologically', 'por', 'infectious', 'la', 'extensively', 'lego', 'mics', 'soul', 've', 'oviparous', 'stocking', 'artists', 'activates']

**Poor**

['82', 'disadvantaged', 'gains', 'economically', 'maximum', 'utility', 'upper', 'aids', 'oxygen', 'covid-19', 'district', 'scramble', 'dry', 'rural', 'demographic', 'reservation', 'descent', 'aged', 'inches', 'northern', 'rising', 'delays', 'assessable', 'bus', 'extends', 'statewide', 'households', 'equitable', 'sheltered', 'ranges', 'productivity', 'immigrated', 'disability', 'severely', 'socioeconomic', 'valley', 'unorganized', 'disabled', 'fluidly', 'pandemic', 'shortage', '6-', 'aide', 'freezing', 'higher', 'inequities', 'increases', 'mountain', 'paraprofessional', '$', 'ranch', 'prediction', 'divided', 'average', 'reteach', 'dependent', 'takers', 'affluent', 'locate', 'million', 'unemployment', 'enrollment', '75', 'lowest', 'dreaded', 'hyperactivity', 'reunite', 'population', 'districts', 'reduces', 'street', 'deficit', '1/2', 'isn', 'rate', 'discrimination', 'epidemic', 'low', 'aloud\u200b', 'bias', 'severity', 'exceptionalities', 'departmentalized', 'exacerbated', 'exceed', 'resort', 'connectable', '64', 'afar', 'percent', 'income', 'loans', 'worker', 'burden', 'poverty', '%', 'disparities', 'of\u200b', 'playdough', '\u200band']

**Extracurricular (ext)**

`Test Loss: 0.491 | Test Acc: 74.86%`

**Rich**

['ozobot', '\u200bparent', '200hr', 'an\u200b', 'bravery', 'gravitates', 'convergent', '®', 'programmable', 'comfortability', 'graphs', 'firsties', 'alouds', 'transformations', 'unifix', 'rectangular', '1:1', '5-', 'florescent', 'laughs', 'transformative', 'thinker', 'neater', 'chunky', 'covid19', 'sharpening', 'drawers', 'transformation', 'believer', 'divergent', 'stretchy', 'four-', 'postage', 'uncharted', 'classroom-', 'impactful', 'rides', 'implements', 'rotations', 'visions', 'pave', 'requests', 'integrates', 'landscapes', 'introduces', 'gun', 'coordinate', 'minifigures', 'coins', 'slinkies', 'cameras', 'seating', 'figurative', 'oh', 'wooden', 'issued', 'login', 'ride', '2/3', 'noisy', 'immersive', 'uniform', 'regression', 'traverse', 'camaraderie', 'goodie', 'paintbrush', 'legibly', 'masterpieces', 'kinetic', 'geometry', 'boots', 'opposed', 'empathetic', 'ancient', '60th', 'covid-19', 'cubes', 'alliance', 'abstract', 'shorter', 'daunting', 'collaborations', 'podcasting', 'segregation', 'prototype', 'shaped', 'cricut', 'makeover', 'coasters', 'robotic', 'receptive', 'charger', 'reclining', 'adapts', 'sleeves', 'shoe', 'ponchos', 'toner', 'reset']

**Poor**

['pandemic', 'sanitary', 'kidney', 'contracting', 'literacy', 'tri', 'living', 'departmentalized', 'housing', 'million', 'severe', 'livelihood', 'wheelchair', 'protection', 'bees', 'boroughs', 'cerebral', 'wipe', 'gently', 'emergencies', 'displaced', 'exceptionalities', 'lowest', 'devastated', 'climate', 'exceeding', 'average', 'rural', 'population', 'dry', 'insurmountable', 'frequency', 'ratio', 'families', 'gallon', 'productivity', '93', 'adjustable', 'students-', 'fell', 'defiant', 'curated', 'expenses', 'price', 'demographic', '600', 'impoverished', 'low', 'melt', 'minority', '5-year', 'land', 'socioeconomic', 'households', 'percent', 'minimum', 'coronavirus', 'handouts', 'ills', 'aids', 'setters', 'excess', 'vulnerable', 'syndrome', 'dysregulated', 'incomes', 'school-', 'reducing', 'hyperactivity', 'rate', 'learnings', '%', 'proportion', 'underprivileged', 'asthma', 'temperatures', 'disadvantaged', 'homelessness', 'palsy', 'desert', 'decompress', 'pollution', 'poorest', 'poverty', 'dollars', 'income', 'skills-', 'rates', 'donor', '-and', 'inequality', 'unemployment', 'injustices', 'neglect', 'on\u200b', 'wage', 'chronic', 'tangrams', 'playstix', 'hardwiring']


**Science (sci)**

`Test Loss: 0.512 | Test Acc: 73.83%`

**Rich**

['exceptionalities', 'cubelets', 'iready', 'fossils', 'code.org', 'hexbugs', 'protein', 'soluble', 'connectors', 'kinesthetically', 'sequence', 'windmill', '7th-', 'playdough', 'beanbag', 'alphabet', 'in\u200b', 'explored', 'yay', 'x', 'brick', 'incorporates', 'responsive', 'cardstock', 'exterior', 'fluorescent', '=', 'stringed', 'displayed', 'linear', 'level-', 'keyboard', 'insects', 'artifacts', 'downloaded', 'budding', 'panels', 'reclining', 'tackling', 'species', 'thematic', '1st', 'tessellating', 'filaments', 'nicely', 'instills', 'holes', 'ah', 'courageous', 'squares', 'finishers', '#', 'quadratic', 'tubes', 'planks', '6th', 'friendships', 'chapter', 'rectangular', '3rd', 'giant', 'literary', 'backdrop', 'renovated', 'brightly', '10th', 'sensor', 'demos', 'disorders', 'trackpad', 'laminate', 'stakes', 'sheet', 'wildlife', 'tissue', 'undergoing', 'covid-19', 'w', 'graph', '8th', 'makey', 'intricate', 'features', 'rechargeable', 'celebration', 'chickens', 'makerspaces', 'makerspace', 'advocacy', 'fascinating', 'sequencing', 'wires', 'playdoh', 'differentiates', 'neon', 'acids', 'adorable', 'tiles', '2nd', 'environmentalists']

**Poor**

['disruption', '$', 'dining', 'pushing', 'rote', 'rent', 'dire', 'pay', 'ha', 'buried', 'schooling', 'breeze', 'west', 'ranches', '800', 'lived', 'unimaginable', 'females', 'serviced', '46', 'valley', 'sickness', 'displaced', 'interruptions', 'limitless', 'handouts', '82', 'shipping', 'heating', 'meals', 'absences', 'homes', 'workforce', 'consequences', 'lunch', 'eats', 'deficit', '45', 'restaurant', 'spheros', 'breakfast', 'rural', 'maneuver', 'poor', '65', 'rising', 'low', 'hardship', 'households', 'population', 'influx', 'families', 'renewable', 'fees', 'pandemic', 'surge', 'velocity', '504s', 'chest', 'meteorological', 'accomodations', 'populated', 'maximum', 'net', 'important\u200b', 'degrees', 'lodging', 'weekday', 'an\u200b', 'percentage', 'looming', 'benefits', 'taxes', 'poorest', 'ozobots', 'accommodations', '66', 'zones', 'winter', 'inequitable', 'reap', 'percent', 'reteaching', '64', 'airfare', 'flooding', 'temperatures', 'exceeding', 'males', 'poverty', '%', 'income', '1.5', 'eaten', 'fell', 'quakes', 'unifix', '..', 'technology/', 'impoverished']


**Arts (arts)**

`Test Loss: 0.550 | Test Acc: 70.84%`

**Rich**

['tubano', '\u200band', '#', 'gallon', 'bin', 'woodwind', 'risers', '16th', 'vs.', 'permanent', 'prom', 'floors', 'phones', 'valve', 'layer', 'architecture', 'festival', 'violin', 'lightweight', 'indoor', 'procedures', 'clarinet', 'earliest', 'win', 'eye', 'piano', '7th', 'mail', 'saxophone', 'rocks', 'equalizer', 'multiage', '8th', 'bells', 'teaches', 'photographers', 'structural', 'emphasis', 'complex', 'landscape', 'cell', 'auditioning', 'tracks', 'motivate', 'wearing', 'symphonic', 'curricular', 'series', 'unit', 'accomplished', 'facilitate', 'drums', 'blues', 'match', 'worlds', 'largest', 'points', 'printmaking', 'stores', 'rhythms', 'chorus', 'futures', 'sketch', 'repairs', 'spaces', '5th', 'decorations', 'film', 'multi', 'orchestra', 'integral', 'pictures', 'sing', 'laugh', 'tempera', 'layering', 'drastically', 'rhythm', 'soar', 'goals', 'photography', 'opens', 'beat', 'cases', 'unprecedented', 'bass', 'camera', 'caddies', 'constant', 'barriers', 'concerts', 'percussion', 'flair', 'tenor', 'commonly', 'relationships', 'mural', 'exploration', 'techniques', 'jazz']

**Poor**

['off', 'navigate', 'trauma', 'representation', 'outdated', 'office', 'conversation', 'spacious', 'ups', 'spots', 'packets', 'damage', 'showing', 'individuality', 'population', 'stuck', 'infectious', 'miss', 'jobs', 'humanity', 'affordable', 'youngest', 'cognitive', 'strokes', 'fantastically', 'autistic', 'backdrops', 'fragile', 'mood', 'childhood', 'outfit', 'written', 'blue', 'stories', 'grows', 'cups', 'rewarding', 'graduation', '/', 'visually', 'crave', 'budgets', 'cushions', 'purchasing', 'tackle', '98', 'functioning', 'board', 'autism', 'notch', 'accompany', 'services', 'breakfast', '60', 'hug', 'emotionally', 'soft', 'scenes', 'coronavirus', 'flag', 'fresh', 'disadvantaged', 'erase', 'living', 'income', 'buckets', 'dry', 'corona', 'distant', 'motivational', 'dire', 'poverty', 'cherish', 'percent', 'soprano', 'adversity', 'fitness', 'd', 'virus', 'pandemic', 'developmental', '..', 'pain', 'shoulder', 'districts', 'ukeleles', 'solvers', 'kinesthetic', 'households', 'county', 'sunny', 'covid-19', 'supplemental', 'warm', 'disabilities', 'portable', 'impairments', 'palette', '%', 'musix']


**Health and Sports (hel)**

`Test Loss: 0.586 | Test Acc: 67.63%`

**Rich**

['exam', 'widen', 'rooms', 'compassionate', 'facts', 'connects', 'educator', 'compassion', '..', 'clues', 'placed', 'notebooks', 'inequity', 'sheets', 'expression', 'completely', 'book', 'creations', 'genres', 'website', 'generational', 'sensory', 'passed', 'edition', 'transgender', 'mathematics', 'narrative', 'texts', 'source', 'habitats', 'formats', 'immigration', 'fiction', 'theme', 'eighth', 'composition', 'disorders', 'identities', 'lifelong', 'selfless', 'super', 'nonfiction', 'atlases', 'teal', 'essays', '-5th', 'efficiency', 'curl', 'pathway', 'answering', '4th', 'edit', '2nd', 'song', 'electronic', 'accomplishements', 'keyboard', 'battles', 'chapter', 'sixth', 'duration', 'trivia', 'll', 'pop', 'covid-19', 'amendment', '7th', 'points', 'graphics', 'cease', 'civic', 'civilizations', 'novel', 'oral', 'version', '8th', 'lyrics', 'coding', 'focal', 'binders', 'cartoon', 'bundle', 'solvers', '*', 'learner', 'visitors', 'publication', 'caution', 'varies', 'celebrates', 'graphic', 'e', 'seamlessly', 'fascinating', '1st', 'retract', 'clicking', 'kick', 'century\u200b', 'read-']

**Poor**

['percent', '%', 'globes', 'households', 'districts', 'departmentalized', 'increases', 'grade\u200b', 'nearby', 'ethnic', '36', '360', 'sticks', 'overnight', 'county', '90', 'outlets', 'predominantly', 'miles', 'digitally', 'fundraiser', 'girl', 'interventions', '60', 'lower', 'hub', 'desk', 'cutter', 'income', 'enforce', 'electric', 'neighborhoods', 'tile', 'poverty', 'district', 'lock', 'laminators', 'attending', 'align', 'aims', 'sharpeners', 'southwestern', 'neighborhood', 'donations', 'enroll', 'cameras', 'universities', 'donating', 'affluent', 'crayons', 'provoke', 'cost', 'responsive', 'urban', 'refugees', 'buy', 'necessities', 'eyed', 'buildings', 'magnet', 'capitals', 'school', 'glue', 'headphone', 'posters', 'supplies', 'hallway', 'diversify', 'population', 'severe', 'suburb', 'household', 'outlet', 'dissidents', 'nations', 'modernize', 'attentive', 'endured', 'rural', 'hardships', 'located', '100', 'region', 'skin', 'units', 'economically', 'creators', '/', 'grateful', 'ports', '97', 'supply', 'interacting', 'supplying', '70', 'eligible', 'foods', 'stores', 'stations', 'cross']


## New Materials

![Category 1](./figures2/category_year.png)

![Category 2](./figures2/category_year2.png)


![Subject 1](./figures2/subject_year.png)

![Subject 2](./figures2/subject_year2.png)

### Category
![Category](./figures2/category_year_pov.png)
![Category](./figures2/category_year_pov_day.png)
![Category](./figures2/category_year_pov_pri.png)
![Category](./figures2/category_year_pov_stu.png)

### Subject
![Subject](./figures2/subject_year_pov.png)
![Subject](./figures2/subject_year_pov_day.png)
![Subject](./figures2/subject_year_pov_pri.png)
![Subject](./figures2/subject_year_pov_stu.png)

### Grade
![Grade Level](./figures2/grd_year_pov.png)
![Grade Level](./figures2/grd_year_pov_day.png)
![Grade Level](./figures2/grd_year_pov_pri.png)
![Grade Level](./figures2/grd_year_pov_stu.png)
