# doccano

doccano is an open source text annotation tool for humans. It provides annotation features for text classification, sequence labeling and sequence to sequence translation. With these features, you can create labeled data for sentiment analysis, named entity recognition, text summarization, and so on. Just create a project, upload some data and start annotating. You can build a dataset in hours.

## Demo

You can enjoy the [annotation demo](http://doccano.herokuapp.com).

### [Named entity recognition](https://doccano.herokuapp.com/demo/named-entity-recognition/)

The first demo is one of the sequence labeling tasks, named-entity recognition. You just select text spans and annotate them. doccano supports shortcut keys, so you can annotate text spans quickly.

![Named Entity Recognition](./docs/named_entity_annotation.gif)

### [Text classification](https://doccano.herokuapp.com/demo/text-classification/)

The second demo is for text classification. Since there may be more than one category, you can annotate with multiple labels. This can also be used for sentiment analysis by creating positive/negative labels.

![Text Classification](./docs/text_classification.gif)

### [Machine translation](https://doccano.herokuapp.com/demo/translation/)

The final demo is one of the sequence to sequence tasks, machine translation. Since there may be more than one responses in sequence to sequence tasks, you can create multiple responses.

![Machine Translation](./docs/translation.gif)

## Features

* Collaborative annotation
* Language independent
* (future) Auto labeling

## Requirements

* Python 3.6+
* django 2.0.5+
* Google Chrome(highly recommended)

## Installation

To install doccano, simply run:

```bash
$ git clone https://github.com/chakki-works/doccano.git
$ cd doccano
$ pip install -r requirements.txt
$ cd app
```

First we’ll need to create a user who can login to the admin site. Run the following command:


```bash
$ python manage.py createsuperuser
```

Enter your desired username and press enter.

```bash
Username: admin
```

You will then be prompted for your desired email address:

```bash
Email address: admin@example.com
```

The final step is to enter your password. You will be asked to enter your password twice, the second time as a confirmation of the first.

```bash
Password: **********
Password (again): *********
Superuser created successfully.
```

## Usage

### Start the development server

Let’s start the development server and explore it.

If the server is not running start it like so:

```bash
$ python manage.py runserver 8080
```

Now, open a Web browser and go to <http://127.0.0.1:8080/login/>. You should see the login screen:

<img src="./docs/login_form.png" alt="Login Form" width=400>

### Create a project

Now, try logging in with the superuser account you created in the previous step. You should see the doccano project list page:

<img src="./docs/projects.png" alt="projects" width=600>

You should see there is no project.

To create your project, make sure you’re in the project list page and select `Create Project` button. You should see the following screen:

<img src="./docs/create_project.png" alt="Project Creation" width=400>

In project creation, you can select three project types: text classification, sequence labeling, or sequence to sequence.

### Import text items

We have now created a project. Now you’re at the “dataset” page for the project. This page displays all the documents in the project. You can see there are no documents.

To import text items, select `Import Data` button in the navigation bar. You should see the following screen:

<img src="./docs/upload.png" alt="Upload project" width=600>

The text items should be provided in txt format. As of now, it must contain only texts. Each line must contain a text:

```python
EU rejects German call to boycott British lamb.
President Obama is speaking at the White House.
He lives in Newark, Ohio.
...
```

Once you select a txt file on your computer, select `Upload` button.

### Define labels

Now we’ll define your labels. To define your labels, select `Labels` menu. You should see the label editor page:

<img src="./docs/label_editor.png" alt="Edit label" width=600>

In label editor page, we can create labels by specifying label text, shortcut key, background color and text color.

### Annotation

Now, we are ready to annotate the texts. Back to the project list page and select the project. You can start annotation!

<img src="./docs/annotation.png" alt="Edit label" width=600>

I hope you are having a great day!

## Contribution

As with any software, doccano is under continuous development. If you have requests for features, please file an issue describing your request. Also, if you want to see work towards a specific feature, feel free to contribute by working towards it. The standard procedure is to fork the repository, add a feature, fix a bug, then file a pull request that your changes are to be merged into the main repository and included in the next release.

## Contact

For help and feedback, please feel free to contact [the author](https://github.com/Hironsan).

**If you are favorite to doccano, please follow my [GitHub](https://github.com/Hironsan) and [Twitter](https://twitter.com/Hironsan13) account.**
