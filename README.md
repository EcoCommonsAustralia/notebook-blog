# EcoCommons Notebook Blog Site Instructions

## Notebook Repos

There are three repositories related to EcoCommons Notebook

1.  EcoCommons/[notebooks](https://github.com/EcoCommonsAustralia/notebooks). This one hosts all the notebook files (ipynb and qmd).
2.  EcoCommons/[notebook-blog](https://github.com/EcoCommonsAustralia/notebook-blog). This one host the site of the notebook blog.
3.  EcoCommons/[ec-notebook_site_materials](https://github.com/EcoCommonsAustralia/ec-notebook_site_materials). This one stores the images used in notebook documents. So that image can be inserted as a github raw link, instead of a file in each notebook folder.

## Notebook Blog Site Repo Files and Folders

| Files/Folders | Description |
|--------------------|----------------------------------------------------|
| ![](https://raw.githubusercontent.com/EcoCommonsAustralia/ec-notebook_site_materials/main/images/folder.svg){width="16"} docs | **The most important folder —** it holds all the HTML files that make up the blog site. This blog is a product of "quarto render'. **Do not change it manually.** |
| ![](https://raw.githubusercontent.com/EcoCommonsAustralia/ec-notebook_site_materials/main/images/folder.svg){width="18"} images | It stores some common images, like EcoCommons logos, etc. |
| ![](https://raw.githubusercontent.com/EcoCommonsAustralia/ec-notebook_site_materials/main/images/folder.svg){width="18"} notebooks | This folder contains all the QMD files of notebooks. This folder should be organised to have the same structures and hierarchy of the blog site's menu. |
| ![](https://raw.githubusercontent.com/EcoCommonsAustralia/ec-notebook_site_materials/main/images/folder.svg){width="18"} styles | Font file and .css file that controls the style of HTMLs. |
| ![](https://raw.githubusercontent.com/EcoCommonsAustralia/ec-notebook_site_materials/main/images/file.svg){width="18"} \_quarto.yml | This controls the structures and the hierarchy of navigation bar, menu, and pages of the blog site. |
| ![](https://raw.githubusercontent.com/EcoCommonsAustralia/ec-notebook_site_materials/main/images/file.svg){width="18"} about.qmd | The about page. |
| ![](https://raw.githubusercontent.com/EcoCommonsAustralia/ec-notebook_site_materials/main/images/file.svg){width="18"} footer.html | The footer section. |
| ![](https://raw.githubusercontent.com/EcoCommonsAustralia/ec-notebook_site_materials/main/images/file.svg){width="18"} index.qmd | The main page. |
| ![](https://raw.githubusercontent.com/EcoCommonsAustralia/ec-notebook_site_materials/main/images/file.svg){width="18"} reference.bib | Reference file. |

## Update Notebook Blog Site

When a new Notebook QMD approved, before merge your branch to the main, we need to update the blog site to create a blog page and get the link of this page.

1.  In the notebook-blog repo Github, create a branch.

2.  Git clone the branch to your local device.

3.  Then in the notebook-blog/notebooks folder, create a sub-folder naming with the notebook.

4.  Copy paste the new approved Notebook QMD to the notebook-blog/notebooks/the-name-of-the-new-notebook folder.

5.  Open terminal, locate to the notebook-blog folder. **Type 'quarto render' and run.** Make sure you are in the level of the notebook-blog folder. If you have not installed quarto, install it first <https://quarto.org/docs/download/>.

    ![](images/clipboard-3747770271.png)

6.  Quarto will render each QMD file and generate a ‘docs’ folder to store all the HTML files that make up the blog site. In general, older notebook QMD files render without issues. If a problem does occur, it is usually caused by a newly added notebook QMD.

![](images/clipboard-3172458001.png){fig-align="center" width="123"}

6.  After rendering is complete, go to notebook-blog/notebook/the-name-of-the-new-notebook folder, add a .gitignore file and add files and folders that you don't want to upload to the Github Repo. For example, large dataset downloaded.

![](images/clipboard-2679938499.png){fig-align="center" width="170"}

7.  Then you can git all changes to your branch. Make make a PR request.

## Tips

1.  If you want to change the foot.html, please go to the https://github.com/EcoCommonsAustralia/ec-notebook_site_materials/blob/main/footer.qmd to download it, make change, and render it to footer.html and replace the old one in this repo.

2.  Try to avoid using/downloading large size of dataset in notebook.

3.  The setting of the Github Pages of the blog site

    ![](images/Screenshot 2025-04-01 at 11.36.07 am.png)
