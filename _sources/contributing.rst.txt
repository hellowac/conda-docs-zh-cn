贡献
============

Contributing

.. _new-issues:

新问题
----------

New Issues

.. tab:: 中文

     如果你遇到的问题是关于以下内容的 bug 报告或功能请求：

     * **某个特定 conda 软件包**：请在 https://github.com/ContinuumIO/anaconda-issues/issues 提交
     * **anaconda.org**：请在 https://github.com/Anaconda-Platform/support/issues 提交
     * **repo.anaconda.com**：请在 https://github.com/ContinuumIO/anaconda-issues/issues 提交
     * ``conda build`` **下的命令**：请在 https://github.com/conda/conda-build/issues 提交
     * ``conda env`` **下的命令**：请在 https://github.com/conda/conda/issues 提交
     * **其他所有 conda 命令**：请在 https://github.com/conda/conda/issues 提交

.. tab:: 英文

     If your issue is a bug report or feature request for:

     * **a specific conda package**: please file it at https://github.com/ContinuumIO/anaconda-issues/issues
     * **anaconda.org**: please file it at https://github.com/Anaconda-Platform/support/issues
     * **repo.anaconda.com**: please file it at https://github.com/ContinuumIO/anaconda-issues/issues
     * **commands under** ``conda build``: please file it at https://github.com/conda/conda-build/issues
     * **commands under** ``conda env``: please file it at https://github.com/conda/conda/issues
     * **all other conda commands**: please file it at https://github.com/conda/conda/issues


开发环境，Bash
-----------------------------

Development Environment, Bash

.. tab:: 中文

     要搭建本地开发环境以参与 conda 的开发，我们推荐如下步骤：
     
     1. Fork `conda/conda` 仓库，并克隆到本地任意目录（一个隔离的 miniconda 环境会在该目录下自动创建），  
        然后设置 ``git remote`` 指向上游仓库和你的 fork。详见下文的详细操作说明。
     
        1a. 选择你希望放置项目的目录位置（不是已有 conda 的位置）
     
        .. code-block:: console
     
            CONDA_PROJECT_ROOT="$HOME/conda"
     
        1b. 克隆项目，设置 ``upstream`` 为主仓库。在 GitHub 页面点击 ``Fork`` 按钮，创建你自己的副本。
     
        .. code-block:: console
     
            GITHUB_USERNAME=kalefranz
            git clone git@github.com:$GITHUB_USERNAME/conda "$CONDA_PROJECT_ROOT"
            cd "$CONDA_PROJECT_ROOT"
            git remote add upstream git@github.com:conda/conda
     
     2. 创建本地开发环境，并激活该环境：
     
        .. code-block:: console
     
            . dev/start
     
        此命令将在 ``./devenv`` 下创建一个特定于该项目的基础环境。  
        如果该环境已存在，命令将直接快速激活已存在的 ``./devenv`` 环境。
     
        要确保当前解释器使用的是项目目录下的 conda 代码，  
        可以通过 ``conda info --all`` 命令输出中的 ``conda location:`` 字段来确认。
     
     3. 使用 GNU make 运行 conda 的单元测试：
     
        .. code-block:: console
     
            make unit
     
        或者，也可以使用 pytest：
     
        .. code-block:: console
     
            py.test -m "not integration and not installed" conda tests
     
        如果你只想运行某个特定测试，也可以这样使用 pytest：
     
        .. code-block:: console
     
            py.test tests/test_create.py -k create_install_update_remove_smoketest

.. tab:: 英文

     To set up an environment to start developing on conda code, we recommend the following steps:
     
     1. Fork the conda/conda repository, clone it locally anywhere you choose (an isolation miniconda
        will be set up within the clone directory), and set up ``git remote`` to point to upstream
        and fork. For detailed directions, see below.
     
        1a. Choose where you want the repository located (not location of existing conda)
     
        .. code-block :: console
     
            CONDA_PROJECT_ROOT="$HOME/conda"
     
        1b. Clone the project, with ``upstream`` being the main repository. Make sure to click the ``Fork``
        button above so you have your own copy of this repo.
     
        .. code-block :: console
     
            GITHUB_USERNAME=kalefranz
            git clone git@github.com:$GITHUB_USERNAME/conda "$CONDA_PROJECT_ROOT"
            cd "$CONDA_PROJECT_ROOT"
            git remote add upstream git@github.com:conda/conda
     
     2. Create a local development environment, and activate that environment
     
        .. code-block :: console
     
            . dev/start
     
        This command will create a project-specific base environment at ``./devenv``. If
        the environment already exists, this command will just quickly activate the
        already-created ``./devenv`` environment.
     
        To be sure that the conda code being interpreted is the code in the project directory,
        look at the value of ``conda location:`` in the output of ``conda info --all``.
     
     3. Run conda's unit tests using GNU make
     
        .. code-block :: console
     
            make unit
     
        or alternately with pytest
     
        .. code-block :: console
     
            py.test -m "not integration and not installed" conda tests
     
        or you can use pytest to focus on one specific test
     
        .. code-block :: console
     
            py.test tests/test_create.py -k create_install_update_remove_smoketest



开发环境，Windows cmd.exe shell
----------------------------------------------

Development Environment, Windows cmd.exe shell

.. tab:: 中文

     上述步骤假设你已安装好 ``git`` 并已加入 ``PATH``。
     
     1. 选择你希望放置项目的目录位置：
     
        .. code-block :: console
     
            set "CONDA_PROJECT_ROOT=%HOMEPATH%\conda"
     
     2. 克隆项目，设置 ``origin`` 为主仓库。请确保点击页面上的 ``Fork`` 按钮，创建你自己的副本：
     
        .. code-block :: console
     
            set GITHUB_USERNAME=kalefranz
            git clone git@github.com:conda/conda "%CONDA_PROJECT_ROOT%"
            cd "%CONDA_PROJECT_ROOT%"
            git remote add %GITHUB_USERNAME% git@github.com:%GITHUB_USERNAME%/conda
     
        要确保当前解释器使用的是项目目录下的 conda 代码，  
        可通过 ``conda info --all`` 输出中的 ``conda location:`` 字段确认。
     
     3. 创建本地开发环境并激活：
     
        .. code-block :: console
      
            .\dev\start
     
        此命令将在 ``.\devenv`` 下创建一个特定于该项目的基础环境。  
        如果该环境已存在，命令将直接激活已存在的 ``.\devenv`` 环境。

.. tab:: 英文

     In these steps, we assume ``git`` is installed and available on ``PATH``.

     1. Choose where you want the project located

        .. code-block :: console
          
             set "CONDA_PROJECT_ROOT=%HOMEPATH%\conda"

     2. Clone the project, with ``origin`` being the main repository. Make sure to click the ``Fork``
        button above so you have your own copy of this repo.

        .. code-block :: console

            set GITHUB_USERNAME=kalefranz
            git clone git@github.com:conda/conda "%CONDA_PROJECT_ROOT%"
            cd "%CONDA_PROJECT_ROOT%"
            git remote add %GITHUB_USERNAME% git@github.com:%GITHUB_USERNAME%/conda

        To be sure that the conda code being interpreted is the code in the project directory,
        look at the value of ``conda location:`` in the output of ``conda info --all``.

     3. Create a local development environment, and activate that environment

        .. code-block :: console

             .\dev\start

        This command will create a project-specific base environment at ``.\devenv``. If
        the environment already exists, this command will just quickly activate the
        already-created ``.\devenv`` environment.


Conda 贡献者许可协议
-----------------------------------

Conda Contributor License Agreement

.. tab:: 中文

     如果你是首次接触 CLA（贡献者许可协议），这在大型开源项目中是非常常见的流程。  
     `Django <https://www.djangoproject.com/foundation/cla/>`_ 和  
     `Python <https://www.python.org/psf/contrib/contrib-form/>`_ 项目都采用了类似机制。

     > CLA 协议的批准最终由人工完成，流程并非完全自动化，  
     
     > 因此你的 PR 上的 CLA 检查可能需要一些时间才能通过。

.. tab:: 英文

     In case you're new to CLAs, this is rather standard procedure for larger projects.
     `Django <https://www.djangoproject.com/foundation/cla/>`_ and even
     `Python <https://www.python.org/psf/contrib/contrib-form/>`_ itself both use something similar.

     > CLA agreements are ultimately approved by a person and are not fully automatic, so it
     
     > may take some time for the CLA checks on your PRs to run successfully.

.. raw:: html

    <iframe src="https://anaconda.na2.echosign.com/public/esignWidget?wid=CBFCIBAA3AAABLblqZhAzPD8JNseGxXBNSY55tQ9ZE65FLEa2B-rUNAEYEjfxph-KGE3uSbu0fvR5cTRRCnY*&hosted=false" width="100%" height="100%" frameborder="0" style="border: 0; overflow: hidden; min-height: 500px; min-width: 600px;"></iframe>
