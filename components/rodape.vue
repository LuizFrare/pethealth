<template>
    <div>
    <footer id="footer">
		<div class="container">
			<div class="row">
				<div class="col-sm-2">
				</div>
				<div class="col-sm-8">
					 <nav>
						<ul id="menu-menu-rodape" class="menu"><li id="menu-item-466" class="menu-item menu-item-type-post_type menu-item-object-page menu-item-has-children menu-item-466"><a class="menu-image-title-after"><span class="menu-image-title-after menu-image-title">{{ $t("footer.specialties.specialtiestext") }}</span></a>
	<ul class="sub-menu">
	<li id="menu-item-467" class="menu-item menu-item-type-post_type_archive menu-item-object-unidades menu-item-467"><NuxtLink to="/caes" class="menu-image-title-after"><span class="menu-image-title-after menu-image-title">{{ $t("footer.specialties.canines") }}</span></NuxtLink></li>
	<li id="menu-item-471" class="menu-item menu-item-type-post_type menu-item-object-page menu-item-471"><NuxtLink to="/gatos" class="menu-image-title-after"><span class="menu-image-title-after menu-image-title">{{ $t("footer.specialties.cats") }}</span></NuxtLink></li>
	<li id="menu-item-474" class="menu-item menu-item-type-post_type menu-item-object-page menu-item-474"><NuxtLink to="/aves" class="menu-image-title-after"><span class="menu-image-title-after menu-image-title">{{ $t("footer.specialties.birds") }}</span></NuxtLink></li>
	</ul>
	</li>
	<li id="menu-item-475" class="menu-item menu-item-type-post_type_archive menu-item-object-exames menu-item-has-children menu-item-475"><a class="menu-image-title-after"><span class="menu-image-title-after menu-image-title">{{ $t("footer.exams.examstext") }}</span></a>
	<ul class="sub-menu">
	<li id="menu-item-476" class="menu-item menu-item-type-post_type menu-item-object-exames menu-item-476"><NuxtLink to="/coletas#laboratorio" class="menu-image-title-after"><span class="menu-image-title-after menu-image-title">{{ $t("footer.exams.laboratory") }}</span></NuxtLink></li>
	<li id="menu-item-477" class="menu-item menu-item-type-post_type menu-item-object-exames menu-item-477"><NuxtLink to="/coletas#vacinas" class="menu-image-title-after"><span class="menu-image-title-after menu-image-title">{{ $t("footer.exams.vaccines") }}</span></NuxtLink></li>
	</ul>
	</li>
	<li id="menu-item-478" class="menu-item menu-item-type-post_type_archive menu-item-object-servicos menu-item-has-children menu-item-478"><a class="menu-image-title-after"><span class="menu-image-title-after menu-image-title">{{ $t("footer.famousraces.famousracestext") }}</span></a>
	<ul class="sub-menu">
	<li id="menu-item-480" class="menu-item menu-item-type-post_type menu-item-object-servicos menu-item-480"><NuxtLink to="/gatos#persa" class="menu-image-title-after"><span class="menu-image-title-after menu-image-title">{{ $t("footer.famousraces.persian") }}</span></NuxtLink></li>
	<li id="menu-item-488" class="menu-item menu-item-type-post_type menu-item-object-servicos menu-item-488"><NuxtLink to="/caes#husky" class="menu-image-title-after"><span class="menu-image-title-after menu-image-title">{{ $t("footer.famousraces.siberianHusky") }}</span></NuxtLink></li>
	</ul>
	</li>
	<li id="menu-item-485" class="menu-item menu-item-type-post_type menu-item-object-page menu-item-has-children menu-item-485"><a class="menu-image-title-after" tag="a"><span class="menu-image-title-after menu-image-title">{{ $t("footer.contact.contacttext") }}</span></a>
	<ul class="sub-menu">
	<li id="menu-item-486" class="menu-item menu-item-type-post_type menu-item-object-page menu-item-486"><NuxtLink to="/contato#formulario" class="menu-image-title-after"><span class="menu-image-title-after menu-image-title">{{ $t("footer.contact.contactus") }}</span></NuxtLink></li>
	<li id="menu-item-12355" class="menu-item menu-item-type-custom menu-item-object-custom menu-item-12355"><NuxtLink to="/contato#vagas" class="menu-image-title-after"><span class="menu-image-title-after menu-image-title">{{ $t("footer.contact.join") }}</span></NuxtLink></li>
	</ul>
	</li>
	</ul>            
	</nav>
				</div>
			</div>
		</div>
	</footer>
	<div class="informacoesContato">
		<p class="TextoInformacoes">{{ $t("footer.subfooter.text1") }}</p>
    <a
    href="#"
    v-for="locale in availableLocales"
    :key="locale.code"
    @click.prevent="switchLocalePatch(locale.code)"
  >
  <img class="bandeira"
          :src="require(`~/static/img/${locale.code}.svg`)"
        />
  </a>
	</div>
    </div>
</template>

<script>
export default {
  computed: {
  availableLocales () {
    return this.$i18n.locales.filter(i => i.code !== this.$i18n.locale)
  },
},
methods: {
  switchLocalePatch(code) {
   this.$i18n.setLocale(code)
  }
}
}
</script>
<style scoped>
/* Rodapé */
#footer {
  background: #0089c9;
  padding-top: 46px;
  padding-bottom: 150px;
  width: 100%;
}

#footer .logo-rodape ul {
  margin: 0px 0 0;
  padding: 0;
}

#footer .logo-rodape ul li {
  display: inline-block;
}

#footer .logo-rodape ul li + li {
  margin-left: 0px
}

#footer nav #menu-menu-rodape {
  margin-bottom: 0;
  padding: 0;
}

@media (max-width: 767px) {
  #footer nav #menu-menu-rodape {
      padding-top: 8px
  }
}

#footer nav #menu-menu-rodape > li {
  width: 25%;
  display: block;
  float: left;
  padding-left: 50px;
  padding-right: 15px
}
@media (max-width: 767px) {
#footer nav #menu-menu-rodape > li {
  width: 25%;
  display: block;
  float: left;
  padding-left: 17px;
  padding-right: 15px
}
}

#footer nav #menu-menu-rodape > li > a {
  font-family: "Nunito";
  font-weight: 700;
  font-size: 18px;
  color: #fff;
}

#footer nav #menu-menu-rodape > li > ul {
  padding-left: 0;
  padding-top: 15px
}

#footer nav #menu-menu-rodape > li > ul > li {
  display: block
}

#footer nav #menu-menu-rodape > li > ul > li > a {
  color: #fff;
  font-family: "Nunito", arial, sans-serif;
  font-size: 14px;
  font-weight: 400
}

#footer nav #menu-menu-rodape > li > ul > li + li {
  padding-top: 11px
}

#footer nav #menu-menu-rodape > li > ul > li > a :hover{
color:#70ecce;
transition: all .5s ease;
}

/* Informações do Rodapé */
.informacoesContato{
padding: 18px 0 14px;
display:block;
height: 100%;
width:100%;
flex: content;
background: #1dbecb;
text-align: center;
}

.TextoInformacoes{
margin: 0;
color: #fff;
font-size: 14px;
font-weight: 600;
font-family: "Nunito";
padding: 7px 50px;
}

/*rodapé responsivo*/
@media (max-width: 767px) {
  #footer {
      padding-top: 41px;
      padding-bottom: 44px;
      width: 100%;
  }
}

@media (max-width: 768px) {
  #footer .logo-rodape > a {
      margin-left: 0;
  }
}

@media (max-width: 767px) {
  #footer nav #menu-menu-rodape > li {
      padding-top: 43px;
  }
}

@media (max-width: 767px) {
  #footer nav #menu-menu-rodape > li {
      width: 100%;
      text-align: center
  }
}

@media (max-width: 767px) {
  #footer nav #menu-menu-rodape > li > a {
      font-size: 26px
  }
}

@media (max-width: 767px) {
  #footer nav #menu-menu-rodape > li > ul {
      padding-top: 10px
  }
}

@media (max-width: 767px) {
  #footer nav #menu-menu-rodape > li > ul > li > a {
      font-size: 22px
  }
}

@media (max-width: 767px) {
  #footer nav #menu-menu-rodape > li > ul > li + li {
      padding-top: 13px
  }
}

.bandeira{
  height: 35px;
}
</style>