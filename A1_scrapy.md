## Information Retrieval - LGLSI2 - Assignment 1 - scrapy

  
**Part I - Scrapy tutorial**

Follow the following tutorial to learn scraping with scrapy

[https://www.youtube.com/watch?v=mBoX_JCKZTE&t=6663s](https://www.youtube.com/watch?v=mBoX_JCKZTE&t=6663s)

The tutorial is about 4h30 long. The mandatory part is until 1h20 while the rest is optional.

Your tasks are:

-   Follow the steps in the tutorial video
-   Apply the steps in a colab notebook then share it on discord #hw2-scrapy-tutorial
      

*Hints*
To run the content of the tutorial on colab, you need to take into consideration the following modifications:
Start the project using the following command:

    !scrapy startproject bookscraper

30 min: To generate a spider inside the spiders folder you need to add a path to the folder as follows:

    !scrapy genspider bookscraper/bookscraper/spiders/bookspider books.toscrape.com

Skip the step “installing ipython”

35 min: the commands entered in the scrapy shell are not visible in colab. Therefore you can use a text editor to write the command then copy paste it to the scrapy shell.

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXe_ar_ViVuy2-_muzni6GQkptkxZkp8mL7uE4DifHZQjj9B5RDKDr8qxboiPvkdZHE0F5_2b0I0UqRcUcZI6_wgSQjRnICG28AK1SJlU_qhQBtZTsy2ySD2bD9OioDY2ilAMDAJ4w?key=F_owuL1rEk0ZxkUqiXRakV1u)

Or you can also change the element type in the page source from “password” to “text” (see screenshots at the end of the assignment).

To run the spider on colab, you first need to access the bookscraper folder:

    %cd bookscraper/bookscraper/

Then save the code as follows:

    %%writefile spiders/bookspider.py

Finally you can start crawling using the following command

    !scrapy crawl bookspider

**Part II - Scraping news websites**

Now you will use scrapy to scrape data from news websites.

Your tasks are:

-   Select at least two news websites (one in Tunisia and outside Tunisia) that you will scrape. 
-   Scrape news data, such as title, text, author, date… 

Later this data will be used to cluster similar news.

**Part III - creating a scrapy tutorial**   

Create a 5min scrapy video tutorial.

  

____________________________________________________________________________

Changing text visibility in scrapy shell

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXcatGIhZUQwJ3jXizWxnV2Y5LNyCv4LcYB5NG86SAqUsoLO-6cakzZ4soKXI_HUr5KUDTpTiOHzOEHCRCfbYpz7JQjQovVql6OgfDaRq6xntRvQ-dCTYK8_aQt4E5Z9eHgv4_MrSw?key=F_owuL1rEk0ZxkUqiXRakV1u)

![](https://lh7-rt.googleusercontent.com/docsz/AD_4nXd6jQW6Oc3RwcM40nItLeeL2TZ3Wbuw5dWk1GEn-Nyrv8b8CAkObXTK4s0sdWk7WMcmTahrMP8bu2UV5tF8wRE7u1Nz5klOHu-BvzEVevMkmIhk3_CKGS-VAumkVKoCvLKz2CCbJQ?key=F_owuL1rEk0ZxkUqiXRakV1u)



