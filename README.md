
# Get Started
1. Please complete [Below assesment](#lwc-and-integration-challenge) upto best of your efforts. Follow the instructions carefully.

## Please login to project using button below. It is a cloud environment with all wheels installed to get started

[![Open in Gitpod](https://gitpod.io/button/open-in-gitpod.svg)](https://contrivers-interview-ck7tsvvc48v.ws-us54.gitpod.io//)
1. Once the terminal pops up, just execute
```bash
sh login.sh
```

# you can clonee this repo and use your local sfdx if configured already 

do it locall by cloning and later pushing code to the repository again. You have been invited to gitlab repository so that you can push your work to repo and submit the assesment when you are ready.

# Guideline
> **VERY IMPORTANT**
>- This Assignment should be completed ONLY in the scratch org that is provided. << Your email >>.json file has sfdxauth url to log you in. steps are also inlined below

1. Don`t stress out to complete. Focus on MUST HAVE, its mandotory. NICE TO HAVE is optional, feel free to complete that too, if you can.
2. For any queries related to assesment or clarifcation required [send your queries to](mailto:tech-assesment-aaaag6vrkwp4er4dwy4aaqvk5i@contrivers.slack.com) tech-assesment-aaaag6vrkwp4er4dwy4aaqvk5i@contrivers.slack.com
or
[Join Slack](https://join.slack.com/share/enQtMzg0MTQyNjY0NjY0MS0wZjc4MjQ0NzE4MGExYzU5MzNiMDM2ZDAwYjM3ZjhhYzEwN2Y2YWIyYjBkOTczOTgzM2NlMTY2NTA1NjI3NTU3) channel to ask
4. When we meet for face to face technical round, we will take this assesment as base and continue discussion from there
5. Please make sure to commit and push to the repo once assesment complete. use conclude.sh script
6. This assignment should be complete in the org created for you. It is 
## All the best! Give your best shot. Looking forward to meet you soon!!
> **IMPORTANT**
>- you will get access to the scratch org which have will expire witihng 30 days. Keep pushing your codebase to remote repo so as not to loose your work.

> **How to login to org - ONLY If doing it locally in your vscode setup. Skip this if you are doing GitPod button above**
>- clone the project locally in vscode
>- the file in this repo <<YOUR_EMAIL.json>> has sfdxauth url that can be used to login
>- sh login.sh
```javascript
sfdx force:auth:sfdxurl:store -f <<your_email>>.json
```
or
```javascript
sh login.sh
```
> **How to submit the assesment**
>- commit the changes with commit message -"Assesement DONE!" & push to repo or notify us via email after pushing your changes
>- the local branch would have created interview/<<< YOUR EMAIL>>>
>- sh conclude.sh

```javascript
sh conclude.sh
```

# LWC and Integration Challenge

## **MUST HAVE**
### **Create a LWC to display a random dog image**

- [Api reference](#get-random-lovely-dog-image)
- onpage load LWC does an API call
- displays a random dog image
- this components should be available in account layout and only loads if account name starts with dog
    * example- User open up an account "CAT", component is **NOT VISIBLE**
    * User opens up an account name DOG Bullodog, component shows random image

### **Create a LWC to display dog image of specific breed in a tile**

- [API reference](#list-all-breeds)
- Create a  LWC app with following features
- Fetch the list of the breed using API call.
- display the name of the breed in center of the tile/lightning card/div
- all tile should be sorted in reverse based on the breed name
- ex- The tile should be ordered like this=> wolfhound, wiffet...bulldog and so on
> **Things To consider**  
>- design the lwC considering the user experience and ease of use
>- Follow best practices for LWC
>- follow best practise for Apex Logic
>- follow best best practise for APEX Rest Integrations
>- be creative to design the UI and lwc
>- The code base should follow DRY principle
>- reusability wherever possible
>

## **NICE TO HAVE**
#### **On click of each tile created in above step to display the image of random dog of selected breed**
- [API reference](#get-dogs-by-breeds)
- get the name of the tile clicked
- pass the name to api [API reference](#get-dogs-by-breeds)
- display random dog image returned in response
#### **A new LwC on Account layout to show random dog image**
- On page load, get the account name
- do api call [API reference](#get-dogs-by-breeds) and pass account name as input
- display if message return with image
- display error notice if no data
  - ex- if account name is CAT the component displays error
- component display image if Account name is -"Bulldog"


> **Things to consider**
>- The code base should follow DRY principle
>- reusability wherever possible



# DOG API

Dog API project sourced from <https://dog.ceo/dog-api/about>

## Documentation

[Documentation](https://dog.ceo/dog-api/documentation/)

<https://dog.ceo>

### **Get random lovely dog image**

```http
  GET /api/breeds/image/random
```

```json
{
    "message": "https://images.dog.ceo/breeds/havanese/00100trPORTRAIT_00100_BURST20191112123933390_COVER.jpg",
    "status": "success"
}
````

### **List All breeds**

```http
  GET /api/breeds/list/all
```

```json
{
    "message": {
        "affenpinscher": [],
        "african": [],
        "airedale": [],
        "akita": [],
        "appenzeller": [],
        "australian": [
            "shepherd"
        ],
        "basenji": [],
        "beagle": [],
        "bluetick": [],
        "borzoi": [],
        "bouvier": [],
        "boxer": [],
        "brabancon": [],
        "briard": [],
        "buhund": [
            "norwegian"
        ],
        "bulldog": [
            "boston",
            "english",
            "french"
        ],
        "bullterrier": [
            "staffordshire"
        ],
        "cattledog": [
            "australian"
        ],
        "chihuahua": [],
        "chow": [],
        "clumber": [],
        "cockapoo": [],
        "collie": [
            "border"
        ],
        "coonhound": [],
        "corgi": [
            "cardigan"
        ],
        "cotondetulear": [],
        "dachshund": [],
        "dalmatian": [],
        "dane": [
            "great"
        ],
        "deerhound": [
            "scottish"
        ],
        "dhole": [],
        "dingo": [],
        "doberman": [],
        "elkhound": [
            "norwegian"
        ],
        "entlebucher": [],
        "eskimo": [],
        "finnish": [
            "lapphund"
        ],
        "frise": [
            "bichon"
        ],
        "germanshepherd": [],
        "greyhound": [
            "italian"
        ],
        "groenendael": [],
        "havanese": [],
        "hound": [
            "afghan",
            "basset",
            "blood",
            "english",
            "ibizan",
            "plott",
            "walker"
        ],
        "husky": [],
        "keeshond": [],
        "kelpie": [],
        "komondor": [],
        "kuvasz": [],
        "labradoodle": [],
        "labrador": [],
        "leonberg": [],
        "lhasa": [],
        "malamute": [],
        "malinois": [],
        "maltese": [],
        "mastiff": [
            "bull",
            "english",
            "tibetan"
        ],
        "mexicanhairless": [],
        "mix": [],
        "mountain": [
            "bernese",
            "swiss"
        ],
        "newfoundland": [],
        "otterhound": [],
        "ovcharka": [
            "caucasian"
        ],
        "papillon": [],
        "pekinese": [],
        "pembroke": [],
        "pinscher": [
            "miniature"
        ],
        "pitbull": [],
        "pointer": [
            "german",
            "germanlonghair"
        ],
        "pomeranian": [],
        "poodle": [
            "medium",
            "miniature",
            "standard",
            "toy"
        ],
        "pug": [],
        "puggle": [],
        "pyrenees": [],
        "redbone": [],
        "retriever": [
            "chesapeake",
            "curly",
            "flatcoated",
            "golden"
        ],
        "ridgeback": [
            "rhodesian"
        ],
        "rottweiler": [],
        "saluki": [],
        "samoyed": [],
        "schipperke": [],
        "schnauzer": [
            "giant",
            "miniature"
        ],
        "setter": [
            "english",
            "gordon",
            "irish"
        ],
        "sharpei": [],
        "sheepdog": [
            "english",
            "shetland"
        ],
        "shiba": [],
        "shihtzu": [],
        "spaniel": [
            "blenheim",
            "brittany",
            "cocker",
            "irish",
            "japanese",
            "sussex",
            "welsh"
        ],
        "springer": [
            "english"
        ],
        "stbernard": [],
        "terrier": [
            "american",
            "australian",
            "bedlington",
            "border",
            "cairn",
            "dandie",
            "fox",
            "irish",
            "kerryblue",
            "lakeland",
            "norfolk",
            "norwich",
            "patterdale",
            "russell",
            "scottish",
            "sealyham",
            "silky",
            "tibetan",
            "toy",
            "welsh",
            "westhighland",
            "wheaten",
            "yorkshire"
        ],
        "tervuren": [],
        "vizsla": [],
        "waterdog": [
            "spanish"
        ],
        "weimaraner": [],
        "whippet": [],
        "wolfhound": [
            "irish"
        ]
    },
    "status": "success"
}
```

### **Get Random Dogs by breeds**

```http
    GET /api/breed/{breed-name}/images/random
```
| Parameter | Type     | Description                       |
| :-------- | :------- | :-------------------------------- |
| `breed-name`      | `string` | **Required**. breed name of the dog. ex- hound |

#### <https://dog.ceo/api/breed/hound/images/random>

```json
{
    "message": "https://images.dog.ceo/breeds/hound-walker/n02089867_1987.jpg",
    "status": "success"
}
```
