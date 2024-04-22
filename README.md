# Examining GPT-4-Turbo's Effectiveness in Matching Reading Levels

## Why It Matters
Before integrating new technology into a sector, it's crucial to tailor it effectively and verify its performance. In the realm of edtech, adjusting AI models to produce content at appropriate reading levels for K-12 education, and consistently measuring these outputs, is essential for their practical application.

## What's Happening
We produced 1600+ passages using OpenAI's GPT-4-Turbo for grades 5 through 12, creating 50 fiction and 50 nonfiction prompts for each grade. Each original passage was then adjusted to match a randomly assigned reading level.

## Data Sources
The original and adjusted texts, spanning grades 5 to 12, were generated via API calls to OpenAI. Each text was crafted to align with specific educational content, and then re-leveled to a different, randomly chosen grade.

## Testing Method
Flesch-Kincaid readability scores are calculated to determine if the AI-generated texts meet the desired complexity for specific grade levels.

## Limitations
This test relied solely on system prompts and final prompts for text generation, without incorporating Retrieval-Augmented Generation (RAG) or other sophisticated methods that might influence the complexity or accuracy of the content.

## Key Findings
- **Complexity Overestimation**: Initial outputs often exhibit complexity levels higher than targeted, suggesting GPT-4-Turbo’s leans towards producing more sophisticated passages than required.
- **Leveled Text Performance**: Even after leveling, texts frequently surpass the intended readability grades.

## Visual Evidence
Scatter plot illustrating the discrepancy between intended and actual Flesch-Kincaid readability levels of generated texts, highlighting complexity overestimations.

## Next Steps
- **Enhanced Contextual Inputs**: We will provide the model with specific guidelines tailored to each grade and passage type (fiction/nonfiction), including word count, sentence structure, vocabulary, and content themes. For instance, for 6th grade, the directives will encompass a word count of 300-375 words, a balanced mix of sentence structures, an introduction to more abstract and nuanced vocabulary, and content that introduces themes and symbolism in stories. This approach is designed to better tailor the generated text to meet the specific requirements of each educational level.
- **Model Self-Adjustment**: We will fine-tune the model using both reading level information and the scores produced by the Flesch-Kincaid readability test, to explore if it can self-adjust and more accurately target the desired complexity levels.
