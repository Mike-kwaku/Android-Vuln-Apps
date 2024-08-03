Author,    Quotes
Mike Lee,                     The best and most beautiful things in the world cannot be seen or even touched - they must be felt with the heart.
James Lee,                    The best preparation for tomorrow is doing your best today.
Sam Lee:,                     Put your heart, mind, and soul into even your smallest acts. This is the secret of success.
John Wee,                     I can't change the direction of the wind, but I can adjust my sails to always reach my destination.
Derrick Lee,                  We must let go of the life we have planned, so as to accept the one that is waiting for us.   


  sentence =    [ 'The best and most beautiful things in the world cannot be seen or even touched - they must be felt with the heart.',
                  'The best preparation for tomorrow is doing your best today.',
                  'Put your heart, mind, and soul into even your smallest acts. This is the secret of success I can't change the direction of the wind 
                  but I can adjust my sails to always reach destination.',
                 'We must let go of the life we have planned, so as to accept the one that is waiting for us.',   
                 'Genius is one percent inspiration and ninety-nine percent perspiration.',
                  'To lead people walk behind them.',
                  'Trouble is only opportunity in work clothes' ]

                  FMGmtPHuF5DeewG7oUANfBGisUlhtlBMIhdRq8R5
uri = "mongodb+srv://aboagyemichaelk:<password>@test.xsb6c76.mongodb.net/?retryWrites=true&w=majority&appName=test"


print(cos_sim(embeddings[0], embeddings[2]))




from sentence_transformers import SentenceTransformer
from sentence_transformers.util import cos_sim
from pymongo import MongoClient
MONGO_CONN_STR = "mongodb+srv://aboagyemichaelk:<password>@test.xsb6c76.mongodb.net/?retryWrites=true&w=majority&appName=test"
mongo_client = MongoClient(MONGO_CONN_STR)
sentences = ['Wisdom is in the sight of him who has understanding',  'The fear of the Lord is the beginning of Wisdom', 'A fool eye wanders on the ends of the earth', 'A fool follows frivolity']
model = SentenceTransformer('thenlper/gte-large')
embeddings = model.encode(sentences)



# Upload documents along with vector embeddings to MongoDB Atlas Collection
output_collection = mongo_client["sample_mflix"]["cohere_embed_movies"]
e = output_collection.insert_many(results)





Start by doing what's necessary; then do what's possible; and suddenly you are doing the impossible.
Happiness is not something you postpone for the future; it is something you design for the present.
It is during our darkest moments that we must focus to see the light.
Try to be a rainbow in someone's cloud.
From a small seed a mighty trunk may grow.
Nothing is impossible, the word itself says 'I'm possible'!
Your work is going to fill a large part of your life, and the only way to be truly satisfied is to do what you believe is great work. And the only way to do great work is to love what you do. If you haven't found it yet, keep looking. Don't settle. As with all matters of the heart, you'll know when you find it.
Change your thoughts and you change your world.
Health is the greatest gift, contentment the greatest wealth, faithfulness the best relationship.
Today I choose life. Every morning when I wake up I can choose joy, happiness, negativity, pain... To feel the freedom that comes from being able to continue to make mistakes and choices - today I choose to feel life, not to deny my humanity but embrace it.
Believe you can and you're halfway there.
My mission in life is not merely to survive, but to thrive; and to do so with some passion, some compassion, some humor, and some style.
No act of kindness, no matter how small, is ever wasted.
Keep your face always toward the sunshine - and shadows will fall behind you.
If opportunity doesn't knock, build a door.
