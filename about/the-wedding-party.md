---
title :  The Wedding Party
layout: page
categories : [about]
resource: true
party:
  - name: "Rose (Maid of Honor)"
    desc: "Rose is lucky enough to be the only person in this group to be related to Amelia. This means that she knows ALL the embarrassing stories - if you're interested please ask. When she's not busy helping Amelia plan the Wedding Of The Year (really, why not) she's raising three amazing kids, baking incredible food and looking for the next book to read."
    align: left
    image: "Rose.jpg"
  - name: "Will Newby"
    desc: "Will has been taking apart computers for playing games with Andre since 2005, even though those computers didn't really start working until 2006 (it was a long process, we broke stuff). Will's still taking things apart and, though he lives in Chicago, still loves Andre and Amelia from afar."
    align: right
    image: "will.jpg"
  - name: "Anna Sahli"
    desc: "Anna met Amelia and Andre at Hamline University, where they quickly became friends discussing Utopias, playing Four Square, and being intimidated by campus squirrels. She generally considers herself the Harry Potter of their magical trio, but has never discussed this with them. She once asked Tonks for her opinion on the matter, but the inquiry was met with aggressive and adorable apathy. Anna joins Amelia and Andre in many happy and themed celebrations, and is looking forward to being a part of their wedding."
    align: left
    image: "anna1.jpg"
  - name: "Alex Sandberg"
    desc: "Alex enjoys playing music, reading, and, thanks to Andre and Amelia, has discovered a taste for sci-fi movies. Yielding to the temptations of schadenfreude, the worse the actors are, the more he likes the movie. Alex has known Andre since second grade, and Amelia since college, and his luck at having these two friends is exceeded only by his happiness for them. Alex lives with his library in Nashville, where he pursues a burgeoning career as an idle recluse."
    align: right
    image: "alex.jpg"
  - name: "Steph Grigsby"
    desc: "Steph is known for her love of candy and cleaning, and is ever so thankful Amelia still wants to remain her friend! Although, she does enjoy other things, such as: reading And movie watching.
Rocking the halls since 6th grade, Amelia and Steph have been through so many fun times and she couldn't be happier for the couple!"
    align: left
    image: "steph.jpg"
  - name: "Kris Frelix"
    desc: "If you're going to be a character there is none better than yourself. I like to believe there's nothing more daring than loving you and surrounding yourself with those who feel the same. Great friends help us play our roles in life and I'm honoured to be around two who are setting their stage and writing a story unlike any other."
    align: right
    image: "kris1.jpg"


---

<!-- FOR LOOP TEST -->
<div class="container">
{% for person in page.party %}

  {% if person.align == 'left' %}
  <div class="row">
    <div class="col-xs-12">
      <h3>
	{{ person.name }}
      </h3>
    </div>
    
    <div class="col-xs-4">
      <a href="https://s3.amazonaws.com/weddednerds.com/{{ person.image }}" class="thumbnail" rel="lightbox-cats">
	<img src="https://s3.amazonaws.com/weddednerds.com/{{ person.image }}" class="img-responsive">
      </a>
    </div>
    
    <div class="col-xs-8">
    {{ person.desc }}
    </div>
  </div>
{% else %}  
  
  <div class="row">
    <div class="col-xs-12">
      <h3>
      {{ person.name }}
      </h3>
    </div>
    
    <div class="col-xs-8">
    {{ person.desc }}
    </div>
    <div class="col-xs-4">
      <a href="https://s3.amazonaws.com/weddednerds.com/{{ person.image }}" class="thumbnail" rel="lightbox-cats">
	<img src="https://s3.amazonaws.com/weddednerds.com/{{ person.image }}" class="img-responsive">
      </a>
    </div>
  </div>
{% endif %}
{% endfor %}
<!-- FOR LOOP TEST -->
</div>


