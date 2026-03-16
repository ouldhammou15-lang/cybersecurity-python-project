# linkedin_demo_cybersecurity.py
# Objectif : Démonstration de compétences en cybersécurité et Python
# Script sûr à partager pour un projet LinkedIn

def check_password_strength(password):
    """
    Vérifie la force d'un mot de passe
    Critères : longueur >=8, majuscules, chiffres, caractères spéciaux
    """
    import re
    length = len(password) >= 8
    upper = re.search(r'[A-Z]', password) is not None
    digit = re.search(r'\d', password) is not None
    special = re.search(r'[!@#$%^&*(),.?":{}|<>]', password) is not None
    
    if all([length, upper, digit, special]):
        return "Mot de passe fort ✅"
    else:
        return "Mot de passe faible ⚠️"

if __name__ == "__main__":
    # Exemple de mots de passe à tester
    passwords = ["Hello123", "Password!", "S3cur3P@ssword"]
    
    for pw in passwords:
        print(f"Mot de passe : {pw} -> {check_password_strength(pw)}")
