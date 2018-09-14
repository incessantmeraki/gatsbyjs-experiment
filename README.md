## Gatsbyjs Experiment

### Part one

- pages reside inside /page
- import Link from 'gatsby-link'
- Normal React thing work 
- gatsby build to produce the final thing
- gatsby develop to run the thing in development mode

### Part two

- Using style={{property: value}} inline
- Using gatsby-plugin-typography to define base typography of site
- applying different theme for typography (/src/utils/typography.js)
- Creating gatsby-config.js (define plugins:[] to load the downloaded plugin)
- Use of CSS in JS (glamor, styled components)
- use of CSS module (file.module.css) which is by default available in gatsby

### Part three

- Applying layout which is common to all pages within gatsby
- Resides in /src/layouts/index.js
- Simple component which accepts props.children and uses it as function call({children()})

### Part four

- Using graphql query to extract data from config file
- export const query = graphql`query find { find { site { siteMetadata { title } }  } }
- using queried data which is available in props.data.site.siteMetadata.title

### Part five

- Use of source plugin to get data into the system
- get information about filesystem using gatsby-source-filesystem

### Part six

- Use of transformer plugin to transform the data received from source plugin
- gatsby-transformer-remark 

### Part Seven

- Generate pages on the plug
- Use of oncreateNode and createPages API from gatbsy in gatsby-node.js to 
- Filter out nodes which are just of type markdown, create their corresponding slug, and make node new node field
- to create page use createPage API to providing the path to the template file (src/templates/blog-post.js)
- above tempalte is provided with slug context which it can use to query for corresponding html
