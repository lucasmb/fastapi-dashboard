<template>
  <div>
    <h1>Posts</h1>
    {{ posts }}
  </div>
</template>

<script>
import { gql } from 'graphql-tag'

export default {
  data() {
    return {
      posts: null,
    }
  },
  apollo: {
    users: gql`
      query {
        posts {
          id
          title
          content
          createdAt
          userId
        }
      }
    `,
  },
}
</script>

<style></style>
