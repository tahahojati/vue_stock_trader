<template>
	<header>
		<nav class="navbar navbar-expand-lg navbar-light bg-light">
		  <router-link class="navbar-brand" to="/">Stock Trader</router-link>
		 <!--  <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
		    <span class="navbar-toggler-icon"></span>
		  </button>
		 -->
		  <div class="collapse navbar-collapse">
		    <ul class="navbar-nav nav mr-auto">
		      <router-link tag="li" to="/portfolio" class="nav-item" activeClass="active">
		        <a class="nav-link">Portfolio </a>
		      </router-link>
		      <router-link tag="li" to="/stocks" class="nav-item" activeClass="active">
		        <a class="nav-link">Stocks</a>
		      </router-link>
		    </ul>
		    <ul class="nav navbar-nav nabar-right">
				<li class="nav-item dropdown">
			        <a class="nav-link dropdown-toggle" href="#" id="navbarDropdown" role="button"
			         data-toggle="dropdown" aria-haspopup="true" aria-expanded="false">
			          Save & Load
			        </a>
			        <div class="dropdown-menu" aria-labelledby="navbarDropdown">
		          		<a class="dropdown-item" href="#">Save Data</a>
			          	<a class="dropdown-item" href="#">Load Data</a>
			        </div>
		      	</li>
		    </ul>
		  </div>
		</nav>
	</header>
</template>