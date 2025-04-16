================
帮助和支持
================

Help and support

社区支持
======================

Community support

.. tab:: 中文

   使用以下工具来提出和回答问题、讨论使用 conda 的方法、请求新功能以及提交您可能有的任何其他评论。
   
   .. grid:: 1 2 2 2
   
     .. grid-item::
   
        .. card:: Conda 社区论坛
           :link: https://conda.discourse.group/
   
           加入我们的 Discourse 论坛，了解 conda 讨论和新闻
   
     .. grid-item::
   
        .. card:: Conda Matrix 聊天
           :link: https://matrix.to/#/#conda:matrix.org
   
           与其他用户讨论 conda 问题和项目
   
     .. grid-item::
   
        .. card:: Anaconda 社区论坛
           :link: https://community.anaconda.cloud/
   
           询问和回答有关 Anaconda 产品的问题

.. tab:: 英文

   Use the following tools to ask and answer questions, discuss ways to use conda,
   request new features, and submit any other comments you might have.
   
   .. grid:: 1 2 2 2
   
     .. grid-item::
   
        .. card:: Conda community forum
           :link: https://conda.discourse.group/
   
           Join our Discourse forum for conda discussion and news
   
     .. grid-item::
   
        .. card:: Conda Matrix chat
           :link: https://matrix.to/#/#conda:matrix.org
   
           Chat about conda issues and projects with other users
   
     .. grid-item::
   
        .. card:: Anaconda community forum
           :link: https://community.anaconda.cloud/
   
           Ask and answer questions about Anaconda's products

付费支持
============

Paid support

.. tab:: 中文

   conda 组织不直接提供 conda 包管理或创建的付费支持、培训或咨询服务。不过，本节列出了提供此类服务的组织。如果您的组织希望加入此列表，请向 `conda-docs 仓库 <https://github.com/conda/conda-docs>`_ 发起拉取请求。

.. tab:: 英文

   The conda organization does not directly offer paid support, training, or consultation on conda package management or creation. However, this section lists organizations that do provide such services. If your organization would like to be added to this list, please open a pull request against the `conda-docs repository <https://github.com/conda/conda-docs>`_.

Anaconda
--------

Anaconda

.. tab:: 中文

   有关其付费支持和咨询计划的信息，请参阅 Anaconda 的 `帮助和支持页面 <https://docs.anaconda.com/reference/help-support/>`__。

.. tab:: 英文

   See Anaconda's `Help and Support page <https://docs.anaconda.com/reference/help-support/>`_ for information on its paid support and consultation programs.

向 GitHub 贡献配方
============================

Contribute recipes to GitHub

.. tab:: 中文

   社区已经过渡到使用 *feedstock* 的方式来管理 conda 包，  
   *feedstock* 是包含软件包配方（recipe）及其构建所需全部配置的代码仓库。  
   通过这种方式，软件包可以借助持续集成（CI）服务实现自动构建。

   你可以从 `Anaconda Recipes <https://github.com/AnacondaRecipes>`_ 克隆或派生（fork）许多软件包的 feedstock，  
   但不能向该 GitHub 组织提交新的 feedstock。  
   如需贡献新的 conda 软件包 feedstock，请通过 Pull Request 的形式提交到以下任一仓库：

   - `conda-forge <https://github.com/conda-forge/staged-recipes>`_  
   - `bioconda <https://github.com/bioconda/bioconda-recipes>`_

   无论使用何种许可证（如 GPL、BSD、MIT 或 Apache），程序的 feedstock 都是受欢迎的。  
   对于已报告的问题，请勿重复提交，若尚未有人报告再提交即可。

   关于 conda 文档的问题可通过 GitHub 进行跟踪：  
   https://github.com/conda/conda-docs/issues

   .. note::

      `conda-docs` 仓库包含 conda 与 conda-build 共享的文档内容，  
      以及这些项目的主页入口文档。

      conda、conda-build 及其他与 conda 相关项目的文档位于各自的代码仓库中。

      若需为 conda、conda-build、repo.anaconda.com、anaconda.org 或特定 conda 软件包提交 issue，  
      请参见贡献指南中的 :ref:`New issues <new-issues>` 部分获取各个项目的仓库链接。

.. tab:: 英文

   The conda community has transitioned into using feedstocks, which
   are repositories that contain package recipes and all of the necessary
   configurations for building those recipes. This enables these packages
   to be automatically built using continuous integration (CI) services.

   You can clone or fork many package feedstocks from `Anaconda Recipes
   <https://github.com/AnacondaRecipes>`_, though you can't submit new
   feedstocks to that GitHub organization. To contribute new conda package
   feedstocks, submit them to `conda-forge
   <https://github.com/conda-forge/staged-recipes>`_ or `bioconda
   <https://github.com/bioconda/bioconda-recipes>`_ with a pull request.

   Feedstocks are welcome for programs that use any license, such as GPL,
   BSD, MIT or Apache, and all of the rt has already been reported,
   and then report it if no one else has.

   Issues with the conda documentation are tracked on GitHub at
   https://github.com/conda/conda-docs/issues.

   .. note::

      The conda-docs repository includes documentation that is common for conda
      and conda-build, as well as landing pages for those projects.

      The documentation for conda, conda-build, and other conda-related
      projects can be found in their respective repositories.

      To create issues for conda, conda-build, repo.anaconda.com, anaconda.org,
      and specific conda packages, please see the individual repo
      links in the :ref:`New issues <new-issues>` section of the Contributing guide.

Conda 公告邮件列表
===========================

Conda Announce mailing list

.. tab:: 中文

   Conda Announce（ `announce@lists.conda.org <https://lists.conda.org/wws/info/announce>`_ ）  
   是一个由 conda 核心团队维护的低频邮件列表，用于发布新闻与更新。  
   这不是营销邮件列表，conda 项目绝不会将你的邮箱出售、转交或分发给第三方。

   * 每周不会超过 1 封邮件，通常更少。
   * 涉及所有 conda 用户的项目公告。
   * 不含企业宣传噱头。
   * 不包含垃圾信息。

   你可以在 `此处订阅 <https://lists.conda.org/wws/subscribe/announce>`__ 。

.. tab:: 英文

   Conda Announce (`announce@lists.conda.org <https://lists.conda.org/wws/info/announce>`_)
   is a low-traffic email list for news and
   updates directly from the conda core team. It
   is not a marketing list. We never sell, give away, or distribute
   your email address to third parties.

   * No more than 1 email per week, usually less.
   * Project announcements relevant to all conda users.
   * No corporate marketing hype.
   * No spam.

   Subscribe `here <https://lists.conda.org/wws/subscribe/announce>`__.
