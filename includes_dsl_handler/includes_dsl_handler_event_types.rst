.. The contents of this file are included in multiple topics.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.


The following table describes the events that may occur during a |chef client| run. Each of these events may be referenced in an ``on`` method block by declaring it as the event type.

.. list-table::
   :widths: 100 420
   :header-rows: 1

   * - Event
     - Description
   * - ``:run_start``
     - The start of the |chef client| run.
   * - ``:run_started``
     - The |chef client| run has started.
   * - ``:ohai_completed``
     - The |ohai| run has completed.
   * - ``:skipping_registration``
     - The |chef client| is not registering with the |chef server| because it already has a private key or because it does not need one.
   * - ``:registration_start``
     - The |chef client| is attempting to create a private key with which to register to the |chef server|.
   * - ``:registration_completed``
     - The |chef client| created its private key successfully.
   * - ``:registration_failed``
     - The |chef client| encountered an error and was unable to register with the |chef server|.
   * - ``:node_load_start``
     - The |chef client| is attempting to load node data from the |chef server|.
   * - ``:node_load_failed``
     - The |chef client| encountered an error and was unable to load node data from the |chef server|.
   * - ``:run_list_expand_failed``
     - The |chef client| failed to expand the run-list.
   * - ``:node_load_completed``
     - The |chef client| successfully loaded node data from the |chef server|. Default and override attributes for roles have been computed, but are not yet applied.
   * - ``:policyfile_loaded``
     - The policy file was loaded.
   * - ``:cookbook_resolution_start``
     - The |chef client| is attempting to pull down the cookbook collection from the |chef server|.
   * - ``:cookbook_resolution_failed``
     - The |chef client| failed to pull down the cookbook collection from the |chef server|.
   * - ``:cookbook_resolution_complete``
     - The |chef client| successfully pulled down the cookbook collection from the |chef server|.
   * - ``:cookbook_clean_start``
     - The |chef client| is attempting to remove unneeded cookbooks.
   * - ``:removed_cookbook_file``
     - The |chef client| removed a file from a cookbook.
   * - ``:cookbook_clean_complete``
     - The |chef client| is done removing cookbooks and/or cookbook files.
   * - ``:cookbook_sync_start``
     - The |chef client| is attempting to synchronize cookbooks.
   * - ``:synchronized_cookbook``
     - The |chef client| is attempting to synchronize the named cookbook.
   * - ``:updated_cookbook_file``
     - The |chef client| updated the named file in the named cookbook.
   * - ``:cookbook_sync_failed``
     - The |chef client| was unable to synchronize cookbooks.
   * - ``:cookbook_sync_complete``
     - The |chef client| is finished synchronizing cookbooks.
   * - ``:library_load_start``
     - The |chef client| is loading library files.
   * - ``:library_file_loaded``
     - The |chef client| successfully loaded the named library file.
   * - ``:library_file_load_failed``
     - The |chef client| was unable to load the named library file.
   * - ``:library_load_complete``
     - The |chef client| is finished loading library files.
   * - ``:lwrp_load_start``
     - The |chef client| is loading custom resources.
   * - ``:lwrp_file_loaded``
     - The |chef client| successfully loaded the named custom resource.
   * - ``:lwrp_file_load_failed``
     - The |chef client| was unable to load the named custom resource.
   * - ``:lwrp_load_complete``
     - The |chef client| is finished loading custom resources.
   * - ``:attribute_load_start``
     - The |chef client| is loading attribute files.
   * - ``:attribute_file_loaded``
     - The |chef client| successfully loaded the named attribute file.
   * - ``:attribute_file_load_failed``
     - The |chef client| was unable to load the named attribute file.
   * - ``:attribute_load_complete``
     - The |chef client| is finished loading attribute files.
   * - ``:definition_load_start``
     - The |chef client| is loading definitions.
   * - ``:definition_file_loaded``
     - The |chef client| successfully loaded the named definition.
   * - ``:definition_file_load_failed``
     - The |chef client| was unable to load the named definition.
   * - ``:definition_load_complete``
     - The |chef client| is finished loading definitions.
   * - ``:recipe_load_start``
     - The |chef client| is loading recipes.
   * - ``:recipe_file_loaded``
     - The |chef client| successfully loaded the named recipe.
   * - ``:recipe_file_load_failed``
     - The |chef client| was unable to load the named recipe.
   * - ``:recipe_not_found``
     - |event_type recipe_not_found|
   * - ``:recipe_load_complete``
     - The |chef client| is finished loading recipes.
   * - ``:converge_start``
     - The |chef client| run converge phase has started.
   * - ``:converge_complete``
     - The |chef client| run converge phase is complete.
   * - ``:converge_failed``
     - |event_type converge_failed|
   * - ``:audit_phase_start``
     - The |chef client| run audit phase has started.
   * - ``:audit_phase_complete``
     - The |chef client| run audit phase is finished.
   * - ``:audit_phase_failed``
     - |event_type audit_phase_failed|
   * - ``:control_group_started``
     - The named control group is being processed.
   * - ``:control_example_success``
     - The named control group has been processed.
   * - ``:control_example_failure``
     - The named control group's processing has failed.
   * - ``:resource_action_start``
     - A resource action is starting.
   * - ``:resource_skipped``
     - A resource action was skipped.
   * - ``:resource_current_state_loaded``
     - A resource's current state was loaded.
   * - ``:resource_current_state_load_bypassed``
     - A resource's current state was not loaded because the resource does not support |whyrun| mode.
   * - ``:resource_bypassed``
     - A resource action was skipped because the resource does not support |whyrun| mode.
   * - ``:resource_update_applied``
     - A change has been made to a resource. (This event occurs for each change made to a resource.)
   * - ``:resource_failed_retriable``
     - A resource action has failed and will be retried.
   * - ``:resource_failed``
     - |event_type resource_failed|
   * - ``:resource_updated``
     - A resource requires modification.
   * - ``:resource_up_to_date``
     - A resource is already correct.
   * - ``:resource_completed``
     - All actions for the resource are complete.
   * - ``:stream_opened``
     - A stream has opened.
   * - ``:stream_closed``
     - A stream has closed.
   * - ``:stream_output``
     - A chunk of data from a single named stream.
   * - ``:handlers_start``
     - The handler processing phase of the |chef client| run has started.
   * - ``:handler_executed``
     - The named handler was processed.
   * - ``:handlers_completed``
     - The handler processing phase of the |chef client| run is complete.
   * - ``:provider_requirement_failed``
     - An assertion declared by a provider has failed.
   * - ``:whyrun_assumption``
     - An assertion declared by a provider has failed, but execution is allowed to continue because the |chef client| is running in |whyrun| mode.
   * - ``:run_completed``
     - The |chef client| run has completed.
   * - ``:run_failed``
     - |event_type run_failed|
