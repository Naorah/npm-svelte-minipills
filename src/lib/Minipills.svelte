<script>
  // src/Minipills.svelte

  // Get all parameters
  export let firstText       = null;
  export let firstTextColor  = null;
  export let firstBgColor    = null;
  export let secondText      = null;
  export let secondTextColor = null;
  export let secondBgColor   = null;
  export let thirdText       = null;
  export let thirdTextColor  = null;
  export let thirdBgColor    = null;
  export let shadows         = null;
  export let logo            = null;
  export let logoColor       = null;
  export let scale           = null;
  export let premade         = null;

  // Whenever parameter changes we update the link again
  $: params = {
    firstText,
    firstTextColor,
    firstBgColor,
    secondText,
    secondTextColor,
    secondBgColor,
    thirdText,
    thirdTextColor,
    thirdBgColor,
    shadows,
    logo,
    logoColor,
    scale,
    premade
  };
  $: if (params) updateLink();

  // basic link
  let link;

  //
  // updateLink : function : update the link to display the minipill
  //
  function updateLink() {
    // baselink for the minipill
    let baseLink = "https://minipills.pelsy.net/pill";

    if (premade) {
      // if it's a premade pill then it's given the priority
      link = `${baseLink}?premade=${premade}`;
    } else {
      // If it's not a premade then we'll take all parameters into account
      let params = new URLSearchParams();
      // Build a parameter store
      params.set('1t', firstText);
      if (firstTextColor) params.set('1c', firstTextColor);
      if (firstBgColor) params.set('1bc', firstBgColor);
      if (secondText) params.set('2t', secondText);
      if (secondTextColor) params.set('2c', secondTextColor);
      if (secondBgColor) params.set('2bc', secondBgColor);
      if (thirdText) params.set('3t', thirdText);
      if (thirdTextColor) params.set('3c', thirdTextColor);
      if (thirdBgColor) params.set('3bc', thirdBgColor);
      if (logo) params.set('l', logo);
      if (logoColor) params.set('lc', logoColor);
      if (shadows) params.set('s', '');
      if (scale) params.set('sc', scale.toString());
      // build the final link
      link = `${baseLink}?${params.toString()}`;
    }
  }
</script>

<img alt="minipill" src={link}>