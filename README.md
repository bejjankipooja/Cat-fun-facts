# Cat-fun-facts
Gen AI workshop
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Cat Facts</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f5f5f5;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
        }

        .container {
            text-align: center;
        }

        button {
            background-color: #8b4513; /* Cat-like brown color */
            color: white;
            border: none;
            padding: 10px 20px;
            margin: 10px;
            cursor: pointer;
            transition: background-color 0.3s ease;
        }

        button:hover {
            background-color: #a0522d; /* Slightly lighter brown */
        }

        .fact-display {
            margin-top: 20px;
            font-size: 1.2em;
            color: #333;
            animation: fadeIn 1s;
        }

        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }

        .twitter-button {
            background-color: #1da1f2; /* Twitter blue */
        }
    </style>
</head>
<body>
    <div class="container">
        <button id="factButton">Show Cat Fact</button>
        <div id="factDisplay" class="fact-display"></div>
        <button id="twitterButton" class="twitter-button">Share to Twitter</button>
    </div>
    <script>
        const facts = [
            "Cats have highly sensitive whiskers that can detect changes in their surroundings, helping them navigate and hunt even in the dark.",
            "While cats often purr when they're happy, they also purr when they're frightened or in pain. The exact reason for purring is still a mystery, but it may help with healing.",
            "Just like human fingerprints, a cat's nose print is unique to each individual cat.",
            "Cats can jump up to six times their body length in one leap, thanks to their powerful leg muscles.",
            "Cats sleep for about 13 to 16 hours a day, which means they spend approximately two-thirds of their life sleeping.",
            "Cats have a wide range of vocalizations, with over 100 different sounds, compared to dogs who have about 10.",
            "Cats were domesticated around 4,000 years ago in ancient Egypt, where they were revered and often associated with the goddess Bastet.",
            "Cats have retractable claws, which helps keep them sharp for hunting and climbing.",
            "Cats have an extraordinary sense of balance, aided by their flexible spine and tail, which helps them land on their feet when they fall.",
            "While cats can't see the full spectrum of colors that humans can, they can see shades of blue and green, and their night vision is far superior to ours."
        ];

        document.getElementById('factButton').addEventListener('click', () => {
            const randomFact = facts[Math.floor(Math.random() * facts.length)];
            document.getElementById('factDisplay').textContent = randomFact;
        });

        document.getElementById('twitterButton').addEventListener('click', () => {
            const text = encodeURIComponent("Generated in GenAI workshop: " + document.getElementById('factDisplay').textContent);
            const url = `https://twitter.com/intent/tweet?text=${text}`;
            window.open(url, '_blank');
        });
    </script>
</body>
</html>

