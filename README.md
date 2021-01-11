# How to publish your own [neuron][1] site

[neuron][2] is a note-taking app optimized for publishing. Use this template repository to get started with [publishing][3] your own neuron site that looks like [one of these][4].

- Go to [https://github.com/srid/neuron-template/generate][5]
- Give your new repository a name, say `mynotes`
- Select "*Include all branches*" ([might be necessary to get the site to publish][6])
- Click "Create repository from template"
  - Note: if you are on the free GitHub plan, your repository should be public for GitHub to publish it.

GitHub will now build the site and serve it at: `https://<yourgithubusername>.github.io/mynotes/`.

For more information, see [neuron documentation][7] as well as the [GitHub Pages guide][8].

## Set your site metadata

- In your new repository, edit the `neuron.dhall` file to set your site configuration (such as title, author, color theme) to suitable values.

## How to edit and add notes

Assuming you have changed the `editUrl` configuration in `neuron.dhall` (see the above section), you can simply click the "edit" icon on the published site to edit any note (see [Editing files in your repository][9] and [Creating new files][10]). On every change, your site should eventually rebuild.

To understand how linking works, read [the neuron guide on Linking][11].

For other ways to edit your notes (editors, web interface), see the [neuron guide][12]. In particular, [Cerveau][13] is the easiest way to edit your notes on the go.

Got questions? Checkout the [[faq]]. To find who else is using this template *publicly on GitHub*, [see here][14].

[1]:	https://neuron.zettel.page/
[2]:	https://neuron.zettel.page/
[3]:	https://neuron.zettel.page/778816d3.html
[4]:	https://neuron.zettel.page/examples.html
[5]:	https://github.com/srid/neuron-template/generate
[6]:	https://stackoverflow.com/a/47368231/55246
[7]:	https://neuron.zettel.page/
[8]:	https://help.github.com/en/github/working-with-github-pages
[9]:	https://help.github.com/en/github/managing-files-in-a-repository/editing-files-in-your-repository
[10]:	https://help.github.com/en/github/managing-files-in-a-repository/creating-new-files
[11]:	https://neuron.zettel.page/linking.html
[12]:	https://neuron.zettel.page/create.html
[13]:	https://www.cerveau.app/
[14]:	https://github.com/search?o=desc&q=filename%3Aneuron.dhall&s=indexed&type=Code

#is_material