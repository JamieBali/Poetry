# N-Gram Poetry Generation

N-grams are super easy ways of generating text. Theoretically an N-Gram system will be able to produce poetry for us if we restrict its actions in a certain way. 
The idea is to make a system which can produce (probably meaningless) poetry that at least fits a structure. If we get that working, we can try and make it generate 
more complex poetry forms, or try to get it to pick a theme.

## Design

To generate poems, we'll use a pair of N-grams (one forward-facing, and one backwards-facing). The forward-facing n-gram can produce lines of text based on the first
word or two, whereas a backwards-facing n-gram can produce lines based on the last words, making it easier to produce rhyming couplets.

## Poetry Styles (and their expected design)

### Tanka

We can start by looking at generating a Tanka - a 31-syllable single sentence poem. This will be the easiest to produce and will act as a simple test to confirm our 
forward-facing n-gram is working fine. We can generate strings of text in single sentences and anything of 31 syllables is technically a Tanka. We can worry about
theme and making the poems make sense later.

### Haiku

A haiku could be generated with the forward facing system too, though this will have per-line syllable counts instead, making it harder to generate. This will be a 
more in-depth test of our syllable counting system, and will allow us to possibly implement a theme-keeping system, ensuring that all lines of the poem are related.

### ABAB Quatrain

An ABAB quatrain is just two rhyming couplets, resulting in 4 lines with no set syllable count. This structure will also be fairly easy to implement, but will work
as a test for our backwards-facing n-gram, and our rhyming system.

### Limerick

A limerick requires rhyming, syllable counts, and thematic consistency, so will be harder to generate once again. We'll be able to use this system to ensure our
backwards-facing n-gram works with the syllable counting and theme keeping systems.

### Sonnet

Assuming the other two systems are working, a sonner shouldn't be too difficult to create. A sonnet is effectively 3 quatrains and a rhyming couplet strung together.
Making a sonnet will allow us to perform a final test on our system, requiring generation of a complex poem requiring rhyming, theme-keeping, and syllable-counting.
