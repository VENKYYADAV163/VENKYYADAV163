## Hi there 👋

<!--
**VENKYYADAV163/VENKYYADAV163** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning Fullstack Python
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->
from django.contrib.auth.models import User
from yourapp.models import Profile

# Find the user
user = User.objects.get(username='Venkateshwarlu')

# Create or update the profile
profile, created = Profile.objects.get_or_create(user=user)
profile.bio = 'This is Venkateshwarlu\'s bio.'
profile.save()
