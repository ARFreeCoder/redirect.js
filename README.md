# redirect.js

<script type='text/javascript'>
  
  //<![CDATA[
  
  // List of unwanted referrer domains
  const blockedReferrers = [
    'google.in'  
  ];

  // Function to extract the domain from a URL
  function extractDomain(url) {
    const a = document.createElement('a');
    a.href = url;
    return a.hostname;
  }

  // Check the referrer and redirect if it matches any blocked domain
  const referrer = document.referrer;
  if (referrer) {
    const referrerDomain = extractDomain(referrer);
    if (blockedReferrers.includes(referrerDomain)) {
      window.location.replace('https://google.com/');
    }
  }

//]]>

</script>

