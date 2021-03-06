# Random Profile Generator [DEMO]

Generates a random user profile with all the common user profile items such as name, address, profile image etc. 
You can generate a complete profile or a generate individual profile properties such as name or address.

[![Build Status](https://kasunkdemos.visualstudio.com/rand-prof-gen/_apis/build/status/halclewis.rand-prof-gen?branchName=master)](https://kasunkdemos.visualstudio.com/rand-prof-gen/_build/latest?definitionId=25?branchName=master)

## Install

Install the package using `npm`
```
npm install random-profile-generator
```

this will install the package to your `node_modules` folder

## Usage

After installing import the package in to your javascript code.

```js
var randomProfile = require('random-profile-generator');
```

# API Documentation

### profile()
Returns a randomly generated user profile with `fullName`, `firstName`, `lastName`, `birthday`, `age`, `avatar`, `address`, `phone`, `email` and `twitter` as properties of the profile object.
Example usage is bellow.

```js
var profile = randomProfile.profile();
console.log(profile);

// Output
/*
{ 
    id: 'dc3800ea-0ae8-592a-bcd6-2012667c3ccc',
    fullName: 'Della Edwards',
    firstName: 'Della',
    lastName: 'Edwards',
    gender: 'Male',
    birthday: 'Mar 24th, 1959',
    age: 57,
    avatar: 'https://api.adorable.io/avatars/200/Della-Edwards',
    address: '49 Foxrun St., Manchester Township, NJ 08759',
    zip: '08759',
    state: 'NJ',
    phone: '(876) 547-1223',
    email: 'cedi@to.cc',
    twitter: '@wunwegda',
    ssn: '744-48-5102'
}
*/
```
Also, profile supports generating `Male` or `Female` profiles by providing an argument. Argument must be `string`.

### Calling with argument `male`
```js
var profile = randomProfile.profile('male');
console.log(profile);

// Output
/*
{ 
    id: '137b6d33-51f2-5994-8250-92667dc5679d',
    fullName: 'Emerson Nicholson', // <= Fullname is MALE name.
    firstName: 'Emerson',
    lastName: 'Nicholson',
    gender: 'Male', // <= Gender is MALE
    birthday: 'Jan 29th, 1965',
    age: 51,
    avatar: 'https://api.adorable.io/avatars/200/Emerson-Nicholson',
    address: '431 Front St., Eastpointe, MI 48021',
    zip: '48021',
    state: 'MI',
    phone: '(362) 561-9961',
    email: 'zu@culdisrik.lk',
    twitter: '@ig',
    ssn: '981-02-7670' 
}
*/
```
### Calling with argument `female`

```js
var profile = randomProfile.profile('female');
console.log(profile);

// Output
/*
{ 
    id: 'b0443ec8-4a00-55aa-8f74-6af0b6c26e17',
    fullName: 'Julie Lewis', // <= Fullname is FEMALE name.
    firstName: 'Julie',
    lastName: 'Lewis',
    gender: 'Female', // <= Gender is FEMALE
    birthday: 'May 15th, 1979',
    age: 37,
    avatar: 'https://api.adorable.io/avatars/200/Julie-Lewis',
    address: '234 E. Bridle Ave., Gloucester, MA 01930',
    zip: '01930',
    state: 'MA',
    phone: '(766) 519-6284',
    email: 'ruszon@mo.et',
    twitter: '@seef',
    ssn: '000-46-2316'
}
*/
```

### name()
Returns a random name with first name and last name. Also can provide `string` arguments `male` or `female` to return a Male or Female name.

```js
var name = randomProfile.name();
console.log(name);

// Output
// => Michael Ruiz

var maleName = randomProfile.name('male');
console.log(maleName);

// Output
// => Emerson Nicholson

var femaleName = randomProfile.name('female');
console.log(femaleName);

// Output
// => Julie Lewis
```

### gender()
Returns a random gender, return value being Male or Female

```js
var gender = randomProfile.gender();
console.log(gender);

// Output
// => Male // or Female
```

### address()
Returns a random address with street, city, State and Zip Code

```js
var address = randomProfile.address();
console.log(address);

// Output
// => 87 North Constitution Circle, Rochester, NY 14606
```

### zip()
Returns a random US Zip code

```js
var zip = randomProfile.zip();
console.log(zip);

// Output
// => 14606
```

### state()
Returns a random 2 letter abbreviation for US state

```js
var state = randomProfile.state();
console.log(state);

// Output
// => NY
```

### birthday()
Returns a random birthday in the `MMM Do[,] YYYY` format.

```js
var birthday = randomProfile.birthday();
console.log(birthday);

// Output
// => Mar 12th, 1991
```

### age()
Returns a random age.

```js
var age = randomProfile.age();
console.log(age);

// Output
// => 25
```

### avatar()
Returns a random avatar url generated from adorable.io API with a 200 x 200px size.

```js
var avatar = randomProfile.avatar();
console.log(avatar);

// Output
// => https://api.adorable.io/avatars/200/Wendy-Conner
```

### phone()
Returns a random phone number with US Phone Number Format.

```js
var phone = randomProfile.phone();
console.log(phone);

// Output
// => (717) 238-3496
```

### email()
Returns a random syntactically valid email address.

```js
var email = randomProfile.email();
console.log(email);

// Output
// => cin@unepwa.cx
```

### ssn()
Returns a random SSN.

```js
var ssn = randomProfile.ssn();
console.log(ssn);

// Output
// => 411-90-0070
```

### twitter()
Returns a random twitter handle.

```js
var twitterHandle = randomProfile.twitter();
console.log(twitterHandle);

// Output
// => @hanaha
```


### guid()
Returns a random GUID.

```js
var guid = randomProfile.guid();
console.log(guid);

// Output
// => b0443ec8-4a00-55aa-8f74-6af0b6c26e17
```

## Installing Dependencies

```sh
# install dependencies listed in package.json
$ npm install
```

## Run Unit Tests Locally

```sh
# Run mocha tests with -w flag
$ npm run test:local
```

# Credits
Random Profile Generator uses some 3rd party packages and APIs for its development. Credit goes to their creators & contributors.

* [Adorable.io]() - Adorable.io API is used to generate the avatar image included in the generated profile.
* [Chancejs](http://chancejs.com/) - Chance is used to generate some of the values found in the generated profile.
* [MomentJs](http://momentjs.com/) - MomentJs is used for some date conversions used in the generated profile.
* [Random Name Generator](http://www.random-name-generator.info/) - Used to generate the random names used in the project.
* [Random Lists](https://www.randomlists.com) - Used to generate the US addresses used in the project.


# License
MIT © [Kasun Kodagoda](http://kasunkodagoda.k2vsoftware.com)

