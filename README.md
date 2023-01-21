## Landing page

### Get started
Learn how to start building, shipping, and maintaining software with GitHub. Explore our products, sign up for an account, and connect with the world's largest development community.

```javascript
import { useEffect, useState } from "react";
import ReactMarkdown from "react-markdown";

const PageComponent = () => {
  const [content, setContent] = useState("");

  useEffect(() => {
    fetch("Page.md")
      .then((res) => res.text())
      .then((text) => setContent(text));
  }, []);

  return (
    <div className="post">
      <ReactMarkdown children={content} />
    </div>
  );
};
```

