~~~xml
<table name="itemRecord">
	<column name="id" primaryKey="true"/>
	<column name="name" type="Varchar" size="255" required="true"/>
	<column name="item" type="Varchar"/>
	<column name="language" type="Varchar"/>
	<column name="excerpt" type="Varchar"/>
	<column name="version" type="Integer"/>
	<column name="left" type="Integer"/>
	<column name="right" type="Integer"/>
	<column name="level" type="Integer"/>
	<column name="thread_id" type="Integer"/>
	<column name="body" type="Integer"/>
	<column name="rank" type="Integer"/>
	<column name="item_id" type="Integer"/>
	<column name="deleted" type="Timestamp"/>
	<column name="url" type="Varchar"/>
	<column name="createdAt" type="Timestamp"/>
	<column name="updatedAt" type="Timestamp"/>
	<unique name="ix_name_ean">
		<unique-column name="name"/>
	</unique>
	<index name="ix_name">
		<index-column name="name"/>
	</index>
	<unique name="ix_ean_publisher"/>
	<index name="ix_name_publisher">
		<index-column name="name"/>
	</index>
	<unique name="IX_UQ_itemRecord_id">
		<unique-column name="id"/>
	</unique>
	<unique name="IX_UQ_itemRecord_name">
		<unique-column name="name"/>
	</unique>
	<behavior name="query_cache">
		<parameter name="backend" value="name"/>
		<parameter name="lifetime" value="600"/>
	</behavior>
	<behavior name="versionable">
		<parameter name="version_column" value="version"/>
		<parameter name="log_created_at" value="true"/>
		<parameter name="log_created_by" value="true"/>
	</behavior>
	<behavior name="nested_set">
		<parameter name="left_column" value="left"/>
		<parameter name="level_column" value="level"/>
		<parameter name="right_column" value="right"/>
		<parameter name="scope_column" value="thread_id"/>
		<parameter name="use_scope" value="true"/>
	</behavior>
	<behavior name="sortable">
		<parameter name="rank_column" value="rank"/>
		<parameter name="scope_column" value="item_id"/>
		<parameter name="use_scope" value="true"/>
	</behavior>
	<behavior name="soft_delete">
		<parameter name="deleted_column" value="deleted"/>
	</behavior>
	<behavior name="sluggable">
		<parameter name="slug_column" value="url"/>
		<parameter name="permanent" value="true"/>
		<parameter name="slug_pattern" value="/items/{name}"/>
		<parameter name="replacement" value="-"/>
		<parameter name="separator" value="/"/>
		<parameter name="replace_pattern" value="/[^\w\/]+/u"/>
	</behavior>
	<behavior name="timestampable">
		<parameter name="create_column" value="createdAt"/>
		<parameter name="update_column" value="updatedAt"/>
		<parameter name="disable_updated_at" value="false"/>
	</behavior>
	<behavior name="aggregate_column">
		<parameter name="name" value="No_of_copies"/>
		<parameter name="expression" value="COUNT (id)"/>
		<parameter name="foreign_table" value="physicalCopy"/>
	</behavior>
	<behavior name="alternative_coding_standards">
		<parameter name="brackets_newline" value="true"/>
		<parameter name="remove_closing_comments" value="true"/>
		<parameter name="strip_comments" value="false"/>
		<parameter name="tab_size" value="2"/>
		<parameter name="use_whitespace" value="true"/>
	</behavior>
	<behavior name="archivable">
		<parameter name="archive_on_insert" value="false"/>
		<parameter name="archive_on_delete" value="false"/>
		<parameter name="archive_on_update" value="false"/>
		<parameter name="archive_class" value="MyBookArchive"/>
		<parameter name="archive_table" value="special_book_archive"/>
		<parameter name="archived_at_column" value="archive_date"/>
		<parameter name="log_archived_at" value="false"/>
	</behavior>
	<behavior name="auto_add_pk">
		<parameter name="type" value="integer"/>
		<parameter name="name" value="id"/>
		<parameter name="autoIncrement" value="true"/>
	</behavior>
	<behavior name=""/>
	<behavior name="i18n">
		<parameter name="i18n_columns" value="item,publisherId"/>
		<parameter name="locale_column" value="language"/>
		<parameter name="i18n_table" value="itemRecord"/>
		<parameter name="default_locale" value="fr_FR"/>
	</behavior>
</table>
~~~