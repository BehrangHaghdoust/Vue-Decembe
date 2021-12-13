<template>
  <div class="home">
    <h1 class="text-center">Home</h1>
    <article v-for="article in articles">
      <h3><a href="`/article/${article.slug}`">{{article.title}}</a></h3>
      <div>{{article.description}} <a href="`/article/${article.slug}`"> + more</a> </div>
      <br>
      <hr>
    </article>

  </div>
</template>

<script>
export default {
  name: "Home",
  data() {
    let articles = localStorage.getItem('articles')
    articles = JSON.parse(articles)
    return {
 articles: articles
    }
  }
};
</script>




// aval ino bord toye localstorage save kard hala ke backend nadarim
baed omad inja pars kardo be array tabdil kard

[
        {
          title: "Title 1",
          slug: "title-1",
          description: ` Lorem ipsum dolor sit amet consectetur, adipisicing elit. At, nulla ab
    doloremque temporibus enim vel voluptatibus ducimus hic sapiente cupiditate
    sit, aliquam repudiandae est qui quisquam itaque neque assumenda
    perspiciatis? Lorem ipsum dolor sit amet consectetur, adipisicing elit. At, nulla ab
    doloremque temporibus enim vel voluptatibus ducimus hic sapiente cupiditate
    sit, aliquam repudiandae est qui quisquam itaque neque assumenda
    perspiciatis?`,
          content: ` Lorem ipsum dolor sit amet consectetur, adipisicing elit. At, nulla ab
    doloremque temporibus enim vel voluptatibus ducimus hic sapiente cupiditate
    sit, aliquam repudiandae est qui quisquam itaque neque assumenda
    perspiciatis? Lorem ipsum dolor sit amet consectetur, adipisicing elit. At, nulla ab
    doloremque temporibus enim vel voluptatibus ducimus hic sapiente cupiditate
    sit, aliquam repudiandae est qui quisquam itaque neque assumenda
    perspiciatis? Lorem ipsum dolor sit amet consectetur, adipisicing elit. At, nulla ab
    doloremque temporibus enim vel voluptatibus ducimus hic sapiente cupiditate
    sit, aliquam repudiandae est qui quisquam itaque neque assumenda
    perspiciatis? Lorem ipsum dolor sit amet consectetur, adipisicing elit. At, nulla ab
    doloremque temporibus enim vel voluptatibus ducimus hic sapiente cupiditate
    sit, aliquam repudiandae est qui quisquam itaque neque assumenda
    perspiciatis? Lorem ipsum dolor sit amet consectetur, adipisicing elit. At, nulla ab
    doloremque temporibus enim vel voluptatibus ducimus hic sapiente cupiditate
    sit, aliquam repudiandae est qui quisquam itaque neque assumenda
    perspiciatis?`,
        },{
          title: "Title 2",
          slug: "title-2",
          description: ` Lorem ipsum dolor sit amet consectetur, adipisicing elit. At, nulla ab
    doloremque temporibus enim vel voluptatibus ducimus hic sapiente cupiditate
    sit, aliquam repudiandae est qui quisquam itaque neque assumenda
    perspiciatis? Lorem ipsum dolor sit amet consectetur, adipisicing elit. At, nulla ab
    doloremque temporibus enim vel voluptatibus ducimus hic sapiente cupiditate
    sit, aliquam repudiandae est qui quisquam itaque neque assumenda
    perspiciatis?`,
          content: ` Lorem ipsum dolor sit amet consectetur, adipisicing elit. At, nulla ab
    doloremque temporibus enim vel voluptatibus ducimus hic sapiente cupiditate
    sit, aliquam repudiandae est qui quisquam itaque neque assumenda
    perspiciatis? Lorem ipsum dolor sit amet consectetur, adipisicing elit. At, nulla ab
    doloremque temporibus enim vel voluptatibus ducimus hic sapiente cupiditate
    sit, aliquam repudiandae est qui quisquam itaque neque assumenda
    perspiciatis? Lorem ipsum dolor sit amet consectetur, adipisicing elit. At, nulla ab
    doloremque temporibus enim vel voluptatibus ducimus hic sapiente cupiditate
    sit, aliquam repudiandae est qui quisquam itaque neque assumenda
    perspiciatis? Lorem ipsum dolor sit amet consectetur, adipisicing elit. At, nulla ab
    doloremque temporibus enim vel voluptatibus ducimus hic sapiente cupiditate
    sit, aliquam repudiandae est qui quisquam itaque neque assumenda
    perspiciatis? Lorem ipsum dolor sit amet consectetur, adipisicing elit. At, nulla ab
    doloremque temporibus enim vel voluptatibus ducimus hic sapiente cupiditate
    sit, aliquam repudiandae est qui quisquam itaque neque assumenda
    perspiciatis?`,
        },{
          title: "Title 3",
          slug: "title-3",
          description: ` Lorem ipsum dolor sit amet consectetur, adipisicing elit. At, nulla ab
    doloremque temporibus enim vel voluptatibus ducimus hic sapiente cupiditate
    sit, aliquam repudiandae est qui quisquam itaque neque assumenda
    perspiciatis? Lorem ipsum dolor sit amet consectetur, adipisicing elit. At, nulla ab
    doloremque temporibus enim vel voluptatibus ducimus hic sapiente cupiditate
    sit, aliquam repudiandae est qui quisquam itaque neque assumenda
    perspiciatis?`,
          content: ` Lorem ipsum dolor sit amet consectetur, adipisicing elit. At, nulla ab
    doloremque temporibus enim vel voluptatibus ducimus hic sapiente cupiditate
    sit, aliquam repudiandae est qui quisquam itaque neque assumenda
    perspiciatis? Lorem ipsum dolor sit amet consectetur, adipisicing elit. At, nulla ab
    doloremque temporibus enim vel voluptatibus ducimus hic sapiente cupiditate
    sit, aliquam repudiandae est qui quisquam itaque neque assumenda
    perspiciatis? Lorem ipsum dolor sit amet consectetur, adipisicing elit. At, nulla ab
    doloremque temporibus enim vel voluptatibus ducimus hic sapiente cupiditate
    sit, aliquam repudiandae est qui quisquam itaque neque assumenda
    perspiciatis? Lorem ipsum dolor sit amet consectetur, adipisicing elit. At, nulla ab
    doloremque temporibus enim vel voluptatibus ducimus hic sapiente cupiditate
    sit, aliquam repudiandae est qui quisquam itaque neque assumenda
    perspiciatis? Lorem ipsum dolor sit amet consectetur, adipisicing elit. At, nulla ab
    doloremque temporibus enim vel voluptatibus ducimus hic sapiente cupiditate
    sit, aliquam repudiandae est qui quisquam itaque neque assumenda
    perspiciatis?`,
        },{
          title: "Title 4",
          slug: "title-4",
          description: ` Lorem ipsum dolor sit amet consectetur, adipisicing elit. At, nulla ab
    doloremque temporibus enim vel voluptatibus ducimus hic sapiente cupiditate
    sit, aliquam repudiandae est qui quisquam itaque neque assumenda
    perspiciatis? Lorem ipsum dolor sit amet consectetur, adipisicing elit. At, nulla ab
    doloremque temporibus enim vel voluptatibus ducimus hic sapiente cupiditate
    sit, aliquam repudiandae est qui quisquam itaque neque assumenda
    perspiciatis?`,
          content: ` Lorem ipsum dolor sit amet consectetur, adipisicing elit. At, nulla ab
    doloremque temporibus enim vel voluptatibus ducimus hic sapiente cupiditate
    sit, aliquam repudiandae est qui quisquam itaque neque assumenda
    perspiciatis? Lorem ipsum dolor sit amet consectetur, adipisicing elit. At, nulla ab
    doloremque temporibus enim vel voluptatibus ducimus hic sapiente cupiditate
    sit, aliquam repudiandae est qui quisquam itaque neque assumenda
    perspiciatis? Lorem ipsum dolor sit amet consectetur, adipisicing elit. At, nulla ab
    doloremque temporibus enim vel voluptatibus ducimus hic sapiente cupiditate
    sit, aliquam repudiandae est qui quisquam itaque neque assumenda
    perspiciatis? Lorem ipsum dolor sit amet consectetur, adipisicing elit. At, nulla ab
    doloremque temporibus enim vel voluptatibus ducimus hic sapiente cupiditate
    sit, aliquam repudiandae est qui quisquam itaque neque assumenda
    perspiciatis? Lorem ipsum dolor sit amet consectetur, adipisicing elit. At, nulla ab
    doloremque temporibus enim vel voluptatibus ducimus hic sapiente cupiditate
    sit, aliquam repudiandae est qui quisquam itaque neque assumenda
    perspiciatis?`,
        },{
          title: "Title 5",
          slug: "title-5",
          description: ` Lorem ipsum dolor sit amet consectetur, adipisicing elit. At, nulla ab
    doloremque temporibus enim vel voluptatibus ducimus hic sapiente cupiditate
    sit, aliquam repudiandae est qui quisquam itaque neque assumenda
    perspiciatis? Lorem ipsum dolor sit amet consectetur, adipisicing elit. At, nulla ab
    doloremque temporibus enim vel voluptatibus ducimus hic sapiente cupiditate
    sit, aliquam repudiandae est qui quisquam itaque neque assumenda
    perspiciatis?`,
          content: ` Lorem ipsum dolor sit amet consectetur, adipisicing elit. At, nulla ab
    doloremque temporibus enim vel voluptatibus ducimus hic sapiente cupiditate
    sit, aliquam repudiandae est qui quisquam itaque neque assumenda
    perspiciatis? Lorem ipsum dolor sit amet consectetur, adipisicing elit. At, nulla ab
    doloremque temporibus enim vel voluptatibus ducimus hic sapiente cupiditate
    sit, aliquam repudiandae est qui quisquam itaque neque assumenda
    perspiciatis? Lorem ipsum dolor sit amet consectetur, adipisicing elit. At, nulla ab
    doloremque temporibus enim vel voluptatibus ducimus hic sapiente cupiditate
    sit, aliquam repudiandae est qui quisquam itaque neque assumenda
    perspiciatis? Lorem ipsum dolor sit amet consectetur, adipisicing elit. At, nulla ab
    doloremque temporibus enim vel voluptatibus ducimus hic sapiente cupiditate
    sit, aliquam repudiandae est qui quisquam itaque neque assumenda
    perspiciatis? Lorem ipsum dolor sit amet consectetur, adipisicing elit. At, nulla ab
    doloremque temporibus enim vel voluptatibus ducimus hic sapiente cupiditate
    sit, aliquam repudiandae est qui quisquam itaque neque assumenda
    perspiciatis?`,
        },{
          title: "Title 6",
          slug: "title-6",
          description: ` Lorem ipsum dolor sit amet consectetur, adipisicing elit. At, nulla ab
    doloremque temporibus enim vel voluptatibus ducimus hic sapiente cupiditate
    sit, aliquam repudiandae est qui quisquam itaque neque assumenda
    perspiciatis? Lorem ipsum dolor sit amet consectetur, adipisicing elit. At, nulla ab
    doloremque temporibus enim vel voluptatibus ducimus hic sapiente cupiditate
    sit, aliquam repudiandae est qui quisquam itaque neque assumenda
    perspiciatis?`,
          content: ` Lorem ipsum dolor sit amet consectetur, adipisicing elit. At, nulla ab
    doloremque temporibus enim vel voluptatibus ducimus hic sapiente cupiditate
    sit, aliquam repudiandae est qui quisquam itaque neque assumenda
    perspiciatis? Lorem ipsum dolor sit amet consectetur, adipisicing elit. At, nulla ab
    doloremque temporibus enim vel voluptatibus ducimus hic sapiente cupiditate
    sit, aliquam repudiandae est qui quisquam itaque neque assumenda
    perspiciatis? Lorem ipsum dolor sit amet consectetur, adipisicing elit. At, nulla ab
    doloremque temporibus enim vel voluptatibus ducimus hic sapiente cupiditate
    sit, aliquam repudiandae est qui quisquam itaque neque assumenda
    perspiciatis? Lorem ipsum dolor sit amet consectetur, adipisicing elit. At, nulla ab
    doloremque temporibus enim vel voluptatibus ducimus hic sapiente cupiditate
    sit, aliquam repudiandae est qui quisquam itaque neque assumenda
    perspiciatis? Lorem ipsum dolor sit amet consectetur, adipisicing elit. At, nulla ab
    doloremque temporibus enim vel voluptatibus ducimus hic sapiente cupiditate
    sit, aliquam repudiandae est qui quisquam itaque neque assumenda
    perspiciatis?`,
        },{
          title: "Title 7",
          slug: "title-7",
          description: ` Lorem ipsum dolor sit amet consectetur, adipisicing elit. At, nulla ab
    doloremque temporibus enim vel voluptatibus ducimus hic sapiente cupiditate
    sit, aliquam repudiandae est qui quisquam itaque neque assumenda
    perspiciatis? Lorem ipsum dolor sit amet consectetur, adipisicing elit. At, nulla ab
    doloremque temporibus enim vel voluptatibus ducimus hic sapiente cupiditate
    sit, aliquam repudiandae est qui quisquam itaque neque assumenda
    perspiciatis?`,
          content: ` Lorem ipsum dolor sit amet consectetur, adipisicing elit. At, nulla ab
    doloremque temporibus enim vel voluptatibus ducimus hic sapiente cupiditate
    sit, aliquam repudiandae est qui quisquam itaque neque assumenda
    perspiciatis? Lorem ipsum dolor sit amet consectetur, adipisicing elit. At, nulla ab
    doloremque temporibus enim vel voluptatibus ducimus hic sapiente cupiditate
    sit, aliquam repudiandae est qui quisquam itaque neque assumenda
    perspiciatis? Lorem ipsum dolor sit amet consectetur, adipisicing elit. At, nulla ab
    doloremque temporibus enim vel voluptatibus ducimus hic sapiente cupiditate
    sit, aliquam repudiandae est qui quisquam itaque neque assumenda
    perspiciatis? Lorem ipsum dolor sit amet consectetur, adipisicing elit. At, nulla ab
    doloremque temporibus enim vel voluptatibus ducimus hic sapiente cupiditate
    sit, aliquam repudiandae est qui quisquam itaque neque assumenda
    perspiciatis? Lorem ipsum dolor sit amet consectetur, adipisicing elit. At, nulla ab
    doloremque temporibus enim vel voluptatibus ducimus hic sapiente cupiditate
    sit, aliquam repudiandae est qui quisquam itaque neque assumenda
    perspiciatis?`
        }
      ]