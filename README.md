# Minipills

@naorah/minipills is a customizable Svelte component for generating pill-style UI elements. This component allows you to create pills with various texts, colors, and sizes, and can include a logo if desired.

## Installation

To install the package, use npm :

```
npm install @naorah/minipills
```

## Usage

To use the Minipills component in your Svelte application, import it and configure it with the available props.

### Basic Usage

```svelte
<script>
  import Minipills from '@naorah/minipills';

  let premade = "minipills";
</script>

<Minipills premade={premade} />
```

## Utils

Some links to help you !

[![To REPL](https://minipills.pelsy.net/pill?1t=Test_on_svelte_REPL&l=svelte&1bc=FF3E00)](https://svelte.dev/repl/db37d20295c44c09971e2b63a68c9895?version=4.2.18)

[![To Website](https://minipills.pelsy.net/pill?1t=Minipills_basement&l=minipills&1bc=A12613)](https://minipills.pelsy.net)

[![To Discord](https://minipills.pelsy.net/pill?1t=Minipills_Discord&l=discord&1bc=5865F2)](https://discord.gg/dSnjfBAaQp)

[![To Github](https://minipills.pelsy.net/pill?1t=To_Github&l=github)](https://github.com/Naorah/npm-svelte-minipills)

## Customization

The Minipills component can be customized using the following props:

- `firstText` (required): The text for the first pill. If it's a double pill, this text appears on the left side.
- `firstTextColor` (optional): The color of the first text. Use a hexadecimal color code without the #. Default is ffffff.
- `firstBgColor` (optional): The background color of the first pill. Use a hexadecimal color code without the #. Default is 212121.
- `secondText` (optional): The text for the second pill.
- `secondTextColor` (optional): The color of the second text. Use a hexadecimal color code without the #. Default is ffffff.
- `secondBgColor` (optional): The background color of the second pill. Use a hexadecimal color code without the #. Default is a12613.
- `thirdText` (optional): The text for the third pill.
- `thirdTextColor` (optional): The color of the third text. Use a hexadecimal color code without the #. Default is ffffff.
- `thirdBgColor` (optional): The background color of the third pill. Use a hexadecimal color code without the #. Default is 212121.
- `shadows` (optional): Enable shadows for the logo and pill text. Set this to true to enable shadows.
- `logo` (optional): A logo to appear in the first part of the pill. Use the simplified text found on the logo page.
- `logoColor` (optional): The color of the logo. Use a hexadecimal color code without the #. Default is ffffff.
- `scale` (optional): The size of the pill. The maximum scale is 10. Default is 1.0.
- `premade` (required): Build a premade pill of the given brand. This parameter takes precedence over all others if provided.

## Example

```svelte
<script>
  import Minipills from '@naorah/minipills';

  let firstText = "Let's go";
  let firstTextColor = "ffffff";
  let firstBgColor = "212121";
  let secondText = "on a road";
  let secondTextColor = "ffffff";
  let secondBgColor = "a12613";
  let thirdText = "trip";
  let thirdTextColor = "ffffff";
  let thirdBgColor = "212121";
  let shadows = true;
  let logo = "minipills";
  let logoColor = "ffffff";
  let scale = 2.0;
  let premade = "";
</script>

<Minipills
  {firstText}
  {firstTextColor}
  {firstBgColor}
  {secondText}
  {secondTextColor}
  {secondBgColor}
  {thirdText}
  {thirdTextColor}
  {thirdBgColor}
  {shadows}
  {logo}
  {logoColor}
  {scale}
  {premade}
/>
```

## License

This project is licensed under the CopyLeft License.