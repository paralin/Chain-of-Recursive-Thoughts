# CoRT (Chain of Recursive Thoughts) 🧠🔄

## TL;DR: I made my AI think harder by making it argue with itself repeatedly. It works stupidly well.

CoRT makes AI models recursively think about their responses, generate alternatives, and pick the best one. It's like giving the AI the ability to doubt itself and try again... and again... and again.

I tested it with Mistral 3.1 24B and it went from "meh" to "holy crap", especially for such a small model, at programming tasks.

## How it works
1. AI generates initial response
2. AI decides how many "thinking rounds" it needs
3. For each round:
   - Generates 3 alternative responses
   - Evaluates all responses
   - Picks the best one
4. Final response is the survivor of this AI battle royale

## Try it yourself
```
pip install -r requirements.txt

# Set one of these API keys
export OPENAI_API_KEY="your-key-here"
# OR
# see: https://github.com/Aider-AI/aider/issues/2227#issuecomment-2869404979
export GITHUB_COPILOT_API_KEY="your-key-here"

python recursive-thinking-ai.py
```

## The Secret Sauce
The magic is in:
- Self-evaluation
- Competitive alternative generation
- Iterative refinement
- Dynamic thinking depth

## License
MIT
