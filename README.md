# react-native-images-collage

[![npm](https://img.shields.io/npm/v/react-native-images-collage.svg?style=flat-square)](https://www.npmjs.com/package/react-native-images-collage)
[![npm licence](http://img.shields.io/npm/l/react-native-images-collage.svg?style=flat-square)](https://npmjs.org/package/react-native-images-collage)
[![npm downloads](http://img.shields.io/npm/dt/react-native-images-collage.svg?style=flat-square)](https://npmjs.org/package/react-native-images-collage)

Customizable image grid component for React Native

![alt text](https://raw.githubusercontent.com/LukeBrandonFarrell/react-native-images-collage/master/collage_1.png)

## Install

To get started install via npm:
```sh
 npm install react-native-images-collage --save
```

## Usage

To use in React Native. Import:
```js
 import { CollageMatrix } from 'react-native-images-collage';
```

Then add this to your code:
```js
<CollageMatrix
  images={ photos }
  matrix={ [ 1, 1, 1, 1 ] }
  direction={ 'row' } />

```

Instead of building your own matrix of collage layouts. There is a JSON file you can import which supports various layouts up to 6 images.
```js
 import { CollageMatrix, LayoutData } from 'react-native-images-collage';
```

You can then access a layout like so:
```js
 LayoutData[NumberOfImages][i]
```

The number in the first bracket will be the configuration you want to access. E.g. configuration for 5 images. The second number is the specific layout you want to access e.g. [2, 2, 1]. You will have to inspect the JSON file to find this out.

## Props

**Note:** For this to work as expected, the number of images has to be equal to the result of all numbers in the matrix. e.g. if matrix is [ 1, 2, 1 ] there has to be 4 images.  

| Prop            | Type          | Optional  | Default | Description                                                                             |
| --------------- | ------------- | --------- | ------- | --------------------------------------------------------------------------------------- |
| images          | array         | No        |         | Images for the collage.                                                                 |
| matrix          | centered      | No        |         | An array like this [ 1, 1, 1 ] equal to the number of images. Used to define the layout |
| separators      | int           | Yes       | 0       | Amount of space between images.                                                         |
| direction       | string        | Yes       | row     | Direction of the collage: 'row' or 'column'.                                            |
| borders         | int           | Yes       | 4       | Width of borders.                                                                       |
| borderColor     | string        | Yes       | white   | Border colour.                                                                          |
| backgroundColor | string        | Yes       | white   | Background color of collage.                                                            |
| containerStyle  | object        | Optional  | 100%    | Style applied to the container of the collage                                           |

## Examples


## Todo

- [ ] Add examples to README
- [ ] Fix some of the JSON layouts for 5 and 6 images
- [ ] Test on Android

## Contributing

If you want to issue a PR, go ahead ;)

## Authors

* [**Luke Brandon Farrell**](https://lukebrandonfarrell.com/) - *Author*

## License

This project is licensed under the MIT License
