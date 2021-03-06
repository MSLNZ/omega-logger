The files in the ``boilerplate`` directory contain the minimum files that
are needed to generate a new ``DatetimeRangePicker`` class.

You can read the `overview <https://dash.plotly.com/react-for-python-developers>`_
for how to create a new Dash Component.

Here are the steps to perform to be able to edit the ``DatetimeRangePicker``
class.

1. Install `Node.js/npm <https://nodejs.org/en/>`_. Open a new terminal so
   that the ``npm`` executable is available on ``PATH``. The following
   should return the version of Node.js packages that are installed::

    npm version

2. Install the Python requirements::

    pip install cookiecutter virtualenv

3. Run cookiecutter on the boilerplate repository::

    cookiecutter https://github.com/plotly/dash-component-boilerplate.git

4. Answer the questions about the project

   * ``project_name``: Set this value to be ``datetime_range_picker``
   * ... enter whatever you want for the other questions ...

5. Copy all files and folders from the ``boilerplate`` directory into the
   `datetime_range_picker` directory that was created by the running the
   `cookiecutter` command. Replace all files when asked.

6. Go to the `datetime_range_picker` directory that was created::

    cd datetime_range_picker
   
   and run the following command to install the missing dependencies::
   
    npm install

7. Activate the virtual environment::

    venv\Scripts\activate

8. Re-build the Dash Component::

    npm run build

   Optional: `moment.js` includes a lot of locales in the `*.min.js` files
   that are automatically generated by running the above command. You can
   delete the unwanted locales in ``node_modules\moment\locale`` to
   exclude those locales from the build. This will reduce the file size.

9. To interact with the ``DatetimeRangePicker`` class run::

     python usage.py
