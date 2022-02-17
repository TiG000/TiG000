<!-- **TiG000/TiG000** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile. -->
### Hi there 👋
#### I am GitHub Readme Generator's creator
![I am GitHub Readme Generator's creator](https://arturssmirnovs.github.io/github-profile-readme-generator/images/banner.png)

I made this project just for fun, it allows you to create nice and simple GitHub Readme files that you can copy/paste and use in your profile.

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
<!-- [![Anurag's GitHub stats](https://github-readme-stats.vercel.app/api?username=TiG000)](https://github.com/anuraghazra/github-readme-stats) -->
![Anurag's GitHub stats](https://github-readme-stats.vercel.app/api?username=TiG000&show_icons=true&theme=prussian)
[![Top Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=TiG000&layout=compact)](https://github.com/anuraghazra/github-readme-stats)


name: Latest blog post workflow
on:
  schedule: # Run workflow automatically
    - cron: '0 * * * *' # Runs every hour, on the hour
  workflow_dispatch: # Run workflow manually (without waiting for the cron to be called), through the Github Actions Workflow page directly
jobs:
  update-readme-with-blog:
    name: Update this repo's README with latest blog posts
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v2
      - uses: gautamkrishnar/blog-post-workflow@master
        with:
          feed_list: "https://KiLien.github.io/index.xml"
