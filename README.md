# typescript_media_query

`typescript_media_query` is a TypeScript library that simplifies handling CSS media queries in web development. It provides a clean, type-safe way to manage and evaluate media queries for responsive designs and dynamic behaviors based on screen size, orientation, and other media features.

## Features
- Type-safe media query handling
- Easy management of responsive designs
- Supports screen size, orientation, and other media features
- Seamlessly integrate media queries directly into TypeScript code

100% typescript support

## Installation

You can install the package using npm or yarn:

```bash



import { useState, useEffect } from "react";

export function useMediaQuery(query: string) {
  const [matches, setMatches] = useState<boolean>(false);

  useEffect(() => {
    const media = window.matchMedia(query);
    const onChange = (event: MediaQueryListEvent) => setMatches(event.matches);

    media.addEventListener("change", onChange);
    setMatches(media.matches);

    return () => media.removeEventListener("change", onChange);
  }, [query]);

  return matches;
}

```




