# MindfulAI-Generative-Art-Therapy-for-Mental-Well-being
MindfulAI combines generative AI and art therapy principles to create personalized, interactive art experiences that promote relaxation, self-expression, and emotional healing.
import requests

# Hypothetical API endpoint for the generative AI art service
ART_GEN_API_URL = "https://api.artgenapi.com/generate"

# Mapping of user moods to art styles
MOOD_TO_ART_STYLE = {
    "happy": "bright and vibrant",
    "sad": "soft and muted",
    "angry": "intense and chaotic",
    "calm": "serene and tranquil"
}

def generate_art_for_mood(mood):
    """
    Generates an art piece based on the user's mood.
    """
    art_style = MOOD_TO_ART_STYLE.get(mood.lower(), "abstract")
    payload = {
        "style": art_style,
        "description": f"Artwork that evokes {mood} mood."
    }
    # Simulate a POST request to the generative AI art API
    # In a real application, this would be an actual request like:
    # response = requests.post(ART_GEN_API_URL, json=payload)
    # Here we'll just pretend we got a response with a URL to the generated art
    response = {
        "status": "success",
        "art_url": f"https://artgenapi.com/generated/{mood}.jpg"
    }
    return response

def main():
    print("Welcome to MindfulAI: Generative Art Therapy for Mental Well-being")
    mood = input("How are you feeling today? (happy, sad, angry, calm): ")
    art_response = generate_art_for_mood(mood)
    
    if art_response["status"] == "success":
        print("Here's a piece of art generated just for you to help with your mood:")
        print(art_response["art_url"])
    else:
        print("Sorry, we couldn't generate art for you at this time. Please try again later.")

if __name__ == "__main__":
    main()
