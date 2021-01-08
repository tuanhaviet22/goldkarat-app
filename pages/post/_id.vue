<template>
  <div class="main-content-wrapper">
    <div class="single-post-area pt--40 pb--80 pt-md--30 pb-md--60">
      <div class="container">
        <div class="row">
          <!-- <div class="col-lg-9 order-lg-2 order-1 mb-md--30"> -->
          <div class="col-12 col-md-12 order-lg-2 order-1 mb-md--30">
            <div class="single-post-wrapper">
              <article class="post post-details mb--30">
                <div class="post-info">
                  <header class="entry-header">
                    <div class="entry-meta">
                                            <span
                                              class="post-date">Đăng lúc: {{}}</span>
                      <span class="post-view">
                                                @for($i =0;$i< $news->post_rate ;$i++)
                                                    <i class="fa fa-star theme-star"></i>
                                                @endfor
                                                &nbsp;&nbsp; Lượt xem: {{ $news->post_view }}
                                            </span>
                    </div>
                    <h1 class="post-title">{!! $news->post_title !!}</h1>
                  </header>
                  <div class="post-content">
                    <p style="word-break: break-all;font-weight: bold;">
                      {!! $sapo !!}
                    </p>
                    @if(!empty($news->post_toc))
                    <div class="toc-block">
                      <div class="title-toc-block">
                        Mục lục bài viết [<span class="btn-hide-toc">ẩn</span>]
                      </div>
                      {!! $news->post_toc !!}
                    </div>
                    @endif
                    {!! $news->post_content !!}
                  </div>
                  <div class="social__sharing mb--30">
                    <ul class="social social-round">
                      <li class="social__item">
                        <iframe
                          src="https://www.facebook.com/plugins/share_button.php?href={{urlencode(url()->current())}}&layout=button_count&size=small&appId=242142420396341&width=119&height=20"
                          width="119" height="20" style="border:none;overflow:hidden"
                          scrolling="no" frameborder="0" allowTransparency="true"
                          allow="encrypted-media"></iframe>
                      </li>
                      <li class="social__item">
                        <div class="zalo-share-button" data-href="{{url()->current()}}"
                             data-oaid="579745863508352884" data-layout="1" data-color="blue"
                             data-customize=false></div>
                      </li>
                    </ul>
                  </div>
                  <div class="footer-meta" style="background-color: white">
                    <div class="fb-comments" data-href="{{url()->current()}}" data-lazy="true"
                         data-numposts="5" data-width="100%"></div>
                  </div>

                </div>
                @if(!empty($relatedPost))
                @if(count($relatedPost) > 0 )
                <section class="blog-area pt--40 pb--40 pt-md--40 pb-md--30">
                  <div class="container">
                    <div class="row">
                      <div class="col-12">
                        <div class="section-title mb--30">
                          <h2>Bài viết liên quan</h2>
                        </div>
                      </div>
                    </div>
                    <div class="row">
                      <div class="col-12">
                        <div class="blog-carousel nav-top slick-item-gutter">
                          @foreach($relatedPost as $post)
                          {!! renderItemPost($post) !!}
                          @endforeach
                        </div>
                      </div>
                    </div>
                  </div>
                </section>
                @endif
                @endif
              </article>
            </div>
          </div>
        </div>
        @if(!empty($relatedProduct))
        @if(count($relatedProduct) > 0)
        <section class="related-products-area pt--80 pb--20 pb-md--15 pt-md--60">
          <div class="row">
            <div class="col-12 mb--20">
              <div class="section-title">
                <h2>Sản phẩm liên quan</h2>
              </div>
            </div>
          </div>
          <div class="row">
            <div class="col-12">
              <div class="product-carousel nav-top js-product-carousel-2">
                @foreach($relatedProduct as $related_product)
                {!! renderItemProduct($related_product) !!}
                @endforeach
              </div>
            </div>
          </div>
        </section>
        @endif
        @endif
        @if(!empty($config_custom->related_image_gallery))
        <section class="related-image-block">
          <div class="section-title">
            <h2>Bộ sưu tập Ảnh liên quan</h2>
          </div>
          <div class="blog-carousel nav-top slick-item-gutter">
            @foreach($related_image_gallery as $key => $gallery)
            {!! renderItemGallery($gallery,$key) !!}
            @endforeach
          </div>
        </section>
        @endif
        @if(!empty($config_custom->related_video_gallery))
        <section class="related-video-block">
          <div class="section-title">
            <h2>Bộ sưu tập Video liên quan</h2>
          </div>
          <div class="blog-carousel nav-top slick-item-gutter">
            @foreach($related_video_gallery as $key => $gallery)
            {!! renderItemGallery($gallery,$key) !!}
            @endforeach
          </div>
        </section>

        @endif
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: '_id',
  data() {
    return {
      idPost: Number,
      dataPost: []
    }
  },
  asyncData({ $axios, route, params }) {
    return $axios.get('/api/post/' + route.params.id).then(response => {
      return {
        dataPost: response.data,
        idPost: route.params.id
      }
    })
  }
}
</script>

<style scoped>

</style>
