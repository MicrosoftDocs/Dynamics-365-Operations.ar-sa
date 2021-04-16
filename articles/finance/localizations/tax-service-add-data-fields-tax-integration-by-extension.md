---
title: أضافه حقول البيانات في تكامل الضريبة باستخدام الملحقات
description: يوضح هذا الموضوع كيفيه استخدام ملحقات X + + لأضافه حقول البيانات في تكامل الضريبة.
author: qire
ms.date: 03/26/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: fdf112bbdd5245d19ab1d07cfcf94c58bf8208c5
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/01/2021
ms.locfileid: "5830330"
---
# <a name="add-data-fields-in-the-tax-integration-by-using-extension"></a><span data-ttu-id="b860f-103">أضافه حقول البيانات في تكامل الضريبة باستخدام الملحقات</span><span class="sxs-lookup"><span data-stu-id="b860f-103">Add data fields in the tax integration by using extension</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="b860f-104">يوضح هذا الموضوع كيفيه استخدام ملحقات X + + لأضافه حقول البيانات في تكامل الضريبة.</span><span class="sxs-lookup"><span data-stu-id="b860f-104">This topic explains how to use X++ extensions to add data fields in the tax integration.</span></span> <span data-ttu-id="b860f-105">يمكن توسيع هذه الحقول إلى نموذج بيانات الضريبة لخدمه الضرائب واستخدامها لتحديد أكواد الضريبة.</span><span class="sxs-lookup"><span data-stu-id="b860f-105">These fields can be extended to the tax data model of the tax service and used to determine tax codes.</span></span> <span data-ttu-id="b860f-106">لمزيد من المعلومات، راجع [أضافه حقول البيانات في تكوينات الضريبة](tax-service-add-data-fields-tax-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="b860f-106">For more information, see [Add data fields in tax configurations](tax-service-add-data-fields-tax-configurations.md).</span></span>

## <a name="data-model"></a><span data-ttu-id="b860f-107">نموذج البيانات</span><span class="sxs-lookup"><span data-stu-id="b860f-107">Data model</span></span>

<span data-ttu-id="b860f-108">يتم تنفيذ البيانات الموجودة في نموذج البيانات بواسطة الكائنات ويتم تنفيذها بواسطة الفئات.</span><span class="sxs-lookup"><span data-stu-id="b860f-108">The data in the data model is carried by objects and implemented by classes.</span></span>

<span data-ttu-id="b860f-109">فيما يلي قائمة بالكائنات الرئيسية:</span><span class="sxs-lookup"><span data-stu-id="b860f-109">Here is a list of the major objects:</span></span>

* <span data-ttu-id="b860f-110">كائن AxClass/TaxIntegration **Document**</span><span class="sxs-lookup"><span data-stu-id="b860f-110">AxClass/TaxIntegration **Document** Object</span></span>
* <span data-ttu-id="b860f-111">كائن AxClass/TaxIntegration **Line**</span><span class="sxs-lookup"><span data-stu-id="b860f-111">AxClass/TaxIntegration **Line** Object</span></span>
* <span data-ttu-id="b860f-112">كائن AxClass/TaxIntegration **TaxLine**</span><span class="sxs-lookup"><span data-stu-id="b860f-112">AxClass/TaxIntegration **TaxLine** Object</span></span>

<span data-ttu-id="b860f-113">يبين الرسم التوضيحي التالي كيفيه ارتباط هذه الكائنات.</span><span class="sxs-lookup"><span data-stu-id="b860f-113">The following illustration shows how these objects are related.</span></span>

<span data-ttu-id="b860f-114">[![علاقة كائن نموذج البيانات](./media/tax-service-customize-image1.png)](./media/tax-service-customize-image1.png)</span><span class="sxs-lookup"><span data-stu-id="b860f-114">[![Data model object relationship](./media/tax-service-customize-image1.png)](./media/tax-service-customize-image1.png)</span></span>

<span data-ttu-id="b860f-115">يمكن أن يحتوي كائن **المستند** على العديد من كائنات **البنود**.</span><span class="sxs-lookup"><span data-stu-id="b860f-115">A **Document** object can contain many **Line** objects.</span></span> <span data-ttu-id="b860f-116">يحتوي كل كائن علي بيانات تعريف لخدمه الضرائب.</span><span class="sxs-lookup"><span data-stu-id="b860f-116">Each object contains metadata for the tax service.</span></span>

- <span data-ttu-id="b860f-117">إن `TaxIntegrationDocumentObject`تحتوي علي `originAddress` بيانات التعريف التي تحتوي علي معلومات حول عنوان المصدر وبيانات تعريف `includingTax`، والتي تشير إلى ما إذا كان مبلغ البند يتضمن ضريبة المبيعات.</span><span class="sxs-lookup"><span data-stu-id="b860f-117">`TaxIntegrationDocumentObject` has `originAddress` metadata, which contains information about the source address, and `includingTax` metadata, which indicates whether the line amount includes sales tax.</span></span>
- <span data-ttu-id="b860f-118">يحتوي `TaxIntegrationLineObject` على بيانات تعريف `itemId`، و`quantity`، و`categoryId`.</span><span class="sxs-lookup"><span data-stu-id="b860f-118">`TaxIntegrationLineObject` has `itemId`, `quantity`, and `categoryId` metadata.</span></span>

> [!NOTE]
> <span data-ttu-id="b860f-119">يقوم `TaxIntegrationLineObject` أيضًا بتطبيق كائنات **التكلفة**.</span><span class="sxs-lookup"><span data-stu-id="b860f-119">`TaxIntegrationLineObject` also implements **Charge** objects.</span></span>

## <a name="integration-flow"></a><span data-ttu-id="b860f-120">سير عمل التكامل</span><span class="sxs-lookup"><span data-stu-id="b860f-120">Integration flow</span></span>

<span data-ttu-id="b860f-121">تتم معالجه البيانات الموجودة في التدفق بواسطة الانشطه.</span><span class="sxs-lookup"><span data-stu-id="b860f-121">The data in the flow is manipulated by activities.</span></span>

### <a name="key-activities"></a><span data-ttu-id="b860f-122">الأنشطة الرئيسية</span><span class="sxs-lookup"><span data-stu-id="b860f-122">Key activities</span></span>

* <span data-ttu-id="b860f-123">AxClass/TaxIntegration **Calculation** ActivityOnDocument</span><span class="sxs-lookup"><span data-stu-id="b860f-123">AxClass/TaxIntegration **Calculation** ActivityOnDocument</span></span>
* <span data-ttu-id="b860f-124">AxClass/TaxIntegration **CurrencyExchange** ActivityOnDocument</span><span class="sxs-lookup"><span data-stu-id="b860f-124">AxClass/TaxIntegration **CurrencyExchange** ActivityOnDocument</span></span>
* <span data-ttu-id="b860f-125">AxClass/TaxIntegration **DataPersistence** ActivityOnDocument</span><span class="sxs-lookup"><span data-stu-id="b860f-125">AxClass/TaxIntegration **DataPersistence** ActivityOnDocument</span></span>
* <span data-ttu-id="b860f-126">AxClass/TaxIntegration **DataRetrieval** ActivityOnDocument</span><span class="sxs-lookup"><span data-stu-id="b860f-126">AxClass/TaxIntegration **DataRetrieval** ActivityOnDocument</span></span>
* <span data-ttu-id="b860f-127">AxClass/TaxIntegration **SettingRetrieval** ActivityOnDocument</span><span class="sxs-lookup"><span data-stu-id="b860f-127">AxClass/TaxIntegration **SettingRetrieval** ActivityOnDocument</span></span>

<span data-ttu-id="b860f-128">يتم تشغيل الانشطه بالترتيب التالي:</span><span class="sxs-lookup"><span data-stu-id="b860f-128">Activities are run in the following order:</span></span>

1. <span data-ttu-id="b860f-129">تعيين الاسترداد</span><span class="sxs-lookup"><span data-stu-id="b860f-129">Setting Retrieval</span></span>
2. <span data-ttu-id="b860f-130">استرداد البيانات</span><span class="sxs-lookup"><span data-stu-id="b860f-130">Data Retrieval</span></span>
3. <span data-ttu-id="b860f-131">خدمه الحساب</span><span class="sxs-lookup"><span data-stu-id="b860f-131">Calculation Service</span></span>
4. <span data-ttu-id="b860f-132">صرف العملة</span><span class="sxs-lookup"><span data-stu-id="b860f-132">Currency Exchange</span></span>
5. <span data-ttu-id="b860f-133">استمرارية البيانات</span><span class="sxs-lookup"><span data-stu-id="b860f-133">Data Persistence</span></span>

<span data-ttu-id="b860f-134">على سبيل المثال، قم بتوسيع **استرداد البيانات** قبل **خدمة الحساب**.</span><span class="sxs-lookup"><span data-stu-id="b860f-134">For example, extend **Data Retrieval** before **Calculation Service**.</span></span>

#### <a name="data-retrieval-activities"></a><span data-ttu-id="b860f-135">أنشطه استرداد البيانات</span><span class="sxs-lookup"><span data-stu-id="b860f-135">Data Retrieval activities</span></span>

<span data-ttu-id="b860f-136">تسترد أنشطة **استرداد البيانات** البيانات من قاعده البيانات.</span><span class="sxs-lookup"><span data-stu-id="b860f-136">**Data Retrieval** activities retrieve data from the database.</span></span> <span data-ttu-id="b860f-137">وتتوفر المحولات الخاصة بالحركات المختلفة لاسترداد البيانات من جداول حركات مختلفه:</span><span class="sxs-lookup"><span data-stu-id="b860f-137">Adapters for different transactions are available to retrieve data from different transaction tables:</span></span>

- <span data-ttu-id="b860f-138">AxClass/TaxIntegration **PurchTable** DataRetrieval</span><span class="sxs-lookup"><span data-stu-id="b860f-138">AxClass/TaxIntegration **PurchTable** DataRetrieval</span></span>
- <span data-ttu-id="b860f-139">AxClass/TaxIntegration **PurchParmTable** DataRetrieval</span><span class="sxs-lookup"><span data-stu-id="b860f-139">AxClass/TaxIntegration **PurchParmTable** DataRetrieval</span></span>
- <span data-ttu-id="b860f-140">AxClass/TaxIntegration **PurchREQTable** DataRetrieval</span><span class="sxs-lookup"><span data-stu-id="b860f-140">AxClass/TaxIntegration **PurchREQTable** DataRetrieval</span></span>
- <span data-ttu-id="b860f-141">AxClass/TaxIntegration **PurchRFQTable** DataRetrieval</span><span class="sxs-lookup"><span data-stu-id="b860f-141">AxClass/TaxIntegration **PurchRFQTable** DataRetrieval</span></span>
- <span data-ttu-id="b860f-142">AxClass/TaxIntegration **VendInvoiceInfoTable** DataRetrieval</span><span class="sxs-lookup"><span data-stu-id="b860f-142">AxClass/TaxIntegration **VendInvoiceInfoTable** DataRetrieval</span></span>
- <span data-ttu-id="b860f-143">AxClass/TaxIntegration **SalesTable** DataRetrieval</span><span class="sxs-lookup"><span data-stu-id="b860f-143">AxClass/TaxIntegration **SalesTable** DataRetrieval</span></span>
- <span data-ttu-id="b860f-144">AxClass/TaxIntegration **SalesParm** DataRetrieval</span><span class="sxs-lookup"><span data-stu-id="b860f-144">AxClass/TaxIntegration **SalesParm** DataRetrieval</span></span>

<span data-ttu-id="b860f-145">في أنشطة **استرداد البيانات** هذه، يتم نسخ البيانات من قاعده البيانات إلى `TaxIntegrationDocumentObject`و`TaxIntegrationLineObject`.</span><span class="sxs-lookup"><span data-stu-id="b860f-145">In these **Data Retrieval** activities, data is copied from the database to `TaxIntegrationDocumentObject` and `TaxIntegrationLineObject`.</span></span> <span data-ttu-id="b860f-146">نظرًا لأن كل هذه الأنشطة تمتد إلى نفس فئة القالب المجرد، فإن لها طرقًا شائعة.</span><span class="sxs-lookup"><span data-stu-id="b860f-146">Because all these activities extend the same abstract template class, they have common methods.</span></span>

#### <a name="calculation-service-activities"></a><span data-ttu-id="b860f-147">أنشطة خدمة الحساب</span><span class="sxs-lookup"><span data-stu-id="b860f-147">Calculation Service activities</span></span>

<span data-ttu-id="b860f-148">نشاط **خدمه الحساب** هو الارتباط بين الخدمة الضريبية وتكامل الضريبة.</span><span class="sxs-lookup"><span data-stu-id="b860f-148">The **Calculation Service** activity is the link between the tax service and the tax integration.</span></span> <span data-ttu-id="b860f-149">يعد هذا النشاط مسؤولا عن الوظائف التالية:</span><span class="sxs-lookup"><span data-stu-id="b860f-149">This activity is responsible for the following functions:</span></span>

1. <span data-ttu-id="b860f-150">إنشاء الطلب.</span><span class="sxs-lookup"><span data-stu-id="b860f-150">Construct the request.</span></span>
2. <span data-ttu-id="b860f-151">ترحيل الطلب إلى خدمه الضرائب.</span><span class="sxs-lookup"><span data-stu-id="b860f-151">Post the request to the tax service.</span></span>
3. <span data-ttu-id="b860f-152">الحصول علي الاستجابة من خدمه الضرائب.</span><span class="sxs-lookup"><span data-stu-id="b860f-152">Get the response from the tax service.</span></span>
4. <span data-ttu-id="b860f-153">تحليل الاستجابة.</span><span class="sxs-lookup"><span data-stu-id="b860f-153">Parse the response.</span></span>

<span data-ttu-id="b860f-154">سيتم ترحيل حقل البيانات الذي تقوم بإضافته إلى الطلب مع بيانات التعريف الأخرى.</span><span class="sxs-lookup"><span data-stu-id="b860f-154">A data field that you add to the request will be posted together with other metadata.</span></span> 

## <a name="extension-implementation"></a><span data-ttu-id="b860f-155">تطبيق ملحق</span><span class="sxs-lookup"><span data-stu-id="b860f-155">Extension implementation</span></span>

<span data-ttu-id="b860f-156">يوفر هذا المقطع خطوات مفصله تشرح كيفيه تنفيذ الملحق.</span><span class="sxs-lookup"><span data-stu-id="b860f-156">This section provides detailed steps that explain how to implement the extension.</span></span> <span data-ttu-id="b860f-157">إنه يستخدم الأبعاد المالية **مركز التكلفة** و **المشروع** كأمثلة.</span><span class="sxs-lookup"><span data-stu-id="b860f-157">It uses the **Cost center** and **Project** financial dimensions as examples.</span></span>

### <a name="step-1-add-the-data-variable-in-the-object-class"></a><span data-ttu-id="b860f-158">الخطوة 1.</span><span class="sxs-lookup"><span data-stu-id="b860f-158">Step 1.</span></span> <span data-ttu-id="b860f-159">أضافه متغير البيانات في فئة الكائن</span><span class="sxs-lookup"><span data-stu-id="b860f-159">Add the data variable in the object class</span></span>

<span data-ttu-id="b860f-160">تحتوي فئة الكائن على متغير البيانات وطرق الحاصل/المعين للبيانات.</span><span class="sxs-lookup"><span data-stu-id="b860f-160">The object class contains the data variable and getter/setter methods for the data.</span></span> <span data-ttu-id="b860f-161">أضف حقل البيانات إلى إما `TaxIntegrationDocumentObject` أو `TaxIntegrationLineObject` حسب مستوى الحقل.</span><span class="sxs-lookup"><span data-stu-id="b860f-161">Add the data field to either `TaxIntegrationDocumentObject` or `TaxIntegrationLineObject`, depending on the level of the field.</span></span> <span data-ttu-id="b860f-162">يستخدم المثال التالي مستوي البند، ويكون اسم الملف هو `TaxIntegrationLineObject_Extension.xpp`.</span><span class="sxs-lookup"><span data-stu-id="b860f-162">The following example uses the line level, and the file name is `TaxIntegrationLineObject_Extension.xpp`.</span></span>

> [!NOTE]
> <span data-ttu-id="b860f-163">إذا كان حقل البيانات الذي تقوم بإضافته موجودا علي مستوي المستند، فقم بتغيير اسم الملف إلى `TaxIntegrationDocumentObject_Extension.xpp`.</span><span class="sxs-lookup"><span data-stu-id="b860f-163">If the data field that you're adding is at the document level, change the file name to `TaxIntegrationDocumentObject_Extension.xpp`.</span></span>

```X++
[ExtensionOf(classStr(TaxIntegrationLineObject))]
final class TaxIntegrationLineObject_Extension
{
    private OMOperatingUnitNumber costCenter;
    private ProjId projectId;

    /// <summary>
    /// Gets a costCenter.
    /// </summary>
    /// <returns>The cost center.</returns>
    public final OMOperatingUnitNumber getCostCenter()
    {
        return this.costCenter;
    }

    /// <summary>
    /// Sets the cost center.
    /// </summary>
    /// <param name = "_value">The cost center.</param>
    public final void setCostCenter(OMOperatingUnitNumber _value)
    {
        this.costCenter = _value;
    }

    /// <summary>
    /// Gets a project ID.
    /// </summary>
    /// <returns>The project ID.</returns>
    public final ProjId getProjectId()
    {
        return this.projectId;
    }

    /// <summary>
    /// Sets the project ID.
    /// </summary>
    /// <param name = "_value">The project ID.</param>
    public final void setProjectId(ProjId _value)
    {
        this.projectId = _value;
    }
}
```

<span data-ttu-id="b860f-164">تتم إضافة **مركز التكلفة** و **المشروع** كمتغيرات خاصه.</span><span class="sxs-lookup"><span data-stu-id="b860f-164">**Cost center** and **Project** are added as private variables.</span></span> <span data-ttu-id="b860f-165">قم بإنشاء أساليب الحاصل والحقل المعين لحقول البيانات هذه لمعالجه البيانات.</span><span class="sxs-lookup"><span data-stu-id="b860f-165">Create getter and setter methods for these data fields to manipulate the data.</span></span>

### <a name="step-2-retrieve-data-from-the-database"></a><span data-ttu-id="b860f-166">الخطوة 2.</span><span class="sxs-lookup"><span data-stu-id="b860f-166">Step 2.</span></span> <span data-ttu-id="b860f-167">استرداد البيانات من قاعده البيانات</span><span class="sxs-lookup"><span data-stu-id="b860f-167">Retrieve data from the database</span></span>

<span data-ttu-id="b860f-168">حدد الحركة، ثم قم بتوسيع فئات المحول المناسبة لاسترداد البيانات.</span><span class="sxs-lookup"><span data-stu-id="b860f-168">Specify the transaction, and extend the appropriate adapter classes to retrieve the data.</span></span> <span data-ttu-id="b860f-169">علي سبيل المثال، إذا كنت تستخدم حركة **أمر شراء**، فيجب عليك توسيع `TaxIntegrationPurchTableDataRetrieval` و`TaxIntegrationVendInvoiceInfoTableDataRetrieval`.</span><span class="sxs-lookup"><span data-stu-id="b860f-169">For example, if you use a **Purchase order** transaction, you must extend `TaxIntegrationPurchTableDataRetrieval` and `TaxIntegrationVendInvoiceInfoTableDataRetrieval`.</span></span> 

> [!NOTE]
> <span data-ttu-id="b860f-170">`TaxIntegrationPurchParmTableDataRetrieval`موروث من `TaxIntegrationPurchTableDataRetrieval`.</span><span class="sxs-lookup"><span data-stu-id="b860f-170">`TaxIntegrationPurchParmTableDataRetrieval` is inherited from `TaxIntegrationPurchTableDataRetrieval`.</span></span> <span data-ttu-id="b860f-171">ولا ينبغي تغييره إلا إذا كان منطق الجدولين `purchTable` و`purchParmTable` مختلفًا.</span><span class="sxs-lookup"><span data-stu-id="b860f-171">It should not be changed unless the logic of the `purchTable` and `purchParmTable` tables differs.</span></span>

<span data-ttu-id="b860f-172">إذا كان يجب أضافه حقل البيانات لكافة الحركات، قم بتوسيع كافة فئات `DataRetrieval`.</span><span class="sxs-lookup"><span data-stu-id="b860f-172">If the data field should be added for all transactions, extend all `DataRetrieval` classes.</span></span>

<span data-ttu-id="b860f-173">ونظرًا لأن كافة أنشطة **استرداد البيانات** تقوم بتوسيع نفس فئة القالب، فان بني الفئة والمتغيرات والأساليب تكون مشابهة.</span><span class="sxs-lookup"><span data-stu-id="b860f-173">Because all **Data Retrieval** activities extend the same template class, the class structures, variables, and methods are similar.</span></span>

```X++
protected TaxIntegrationDocumentObject document;

/// <summary>
/// Copies to the document.
/// </summary>
protected abstract void copyToDocument()
{
    // It is recommended to implement as:
    //
    // this.copyToDocumentByDefault();
    // this.copyToDocumentFromHeaderTable();
    // this.copyAddressToDocument();
}
 
/// <summary>
/// Copies to the current line of the document.
/// </summary>
/// <param name = "_line">The current line of the document.</param>
protected abstract void copyToLine(TaxIntegrationLineObject _line)
{
    // It is recommended to implement as:
    //
    // this.copyToLineByDefault(_line);
    // this.copyToLineFromLineTable(_line);
    // this.copyQuantityAndTransactionAmountToLine(_line);
    // this.copyAddressToLine(_line);
    // this.copyToLineFromHeaderTable(_line);
}
```

<span data-ttu-id="b860f-174">يوضح المثال التالي البنية الاساسيه عند استخدام جدول `PurchTable`.</span><span class="sxs-lookup"><span data-stu-id="b860f-174">The following example shows the basic structure when the `PurchTable` table is used.</span></span>

```X++
public class TaxIntegrationPurchTableDataRetrieval extends TaxIntegrationAbstractDataRetrievalTemplate
{
    protected PurchTable purchTable;
    protected PurchLine purchLine;

    // Query builder methods
    [Replaceable]
    protected SysDaQueryObject getDocumentQueryObject()
    [Replaceable]
    protected SysDaQueryObject getLineQueryObject()
    [Replaceable]
    protected SysDaQueryObject getDocumentChargeQueryObject()
    [Replaceable]
    protected SysDaQueryObject getLineChargeQueryObject()

    // Data retrieval methods
    protected void copyToDocument()
    protected void copyToDocumentFromHeaderTable()
    protected void copyToLine(TaxIntegrationLineObject _line)
    protected void copyToLineFromLineTable(TaxIntegrationLineObject _line)
    ...
}
```

<span data-ttu-id="b860f-175">عند استدعاء أسلوب `CopyToDocument`، يكون المخزن المؤقت لـ `this.purchTable` موجودًا بالفعل.</span><span class="sxs-lookup"><span data-stu-id="b860f-175">When the `CopyToDocument` method is called, the `this.purchTable` buffer already exists.</span></span> <span data-ttu-id="b860f-176">ويتمثل الغرض من هذه الطريقة في نسخ كافة البيانات المطلوبة من `this.purchTable` إلى كائن `document` باستخدام أسلوب المعين الذي تم إنشاؤه في فئة `DocumentObject`.</span><span class="sxs-lookup"><span data-stu-id="b860f-176">The purpose of this method is to copy all the required data from `this.purchTable` to the `document` object by using the setter method that was created in the `DocumentObject` class.</span></span>

<span data-ttu-id="b860f-177">وبالمثل، يوجد مخزن `this.purchLine` المؤقت بالفعل في أسلوب `CopyToLine`.</span><span class="sxs-lookup"><span data-stu-id="b860f-177">Likewise, a `this.purchLine` buffer already exists in the `CopyToLine` method.</span></span> <span data-ttu-id="b860f-178">ويتمثل الغرض من هذه الطريقة في نسخ كافة البيانات المطلوبة من `this.purchLine` إلى كائن `_line` باستخدام أسلوب المعين الذي تم إنشاؤه في فئة `LineObject`.</span><span class="sxs-lookup"><span data-stu-id="b860f-178">The purpose of this method is to copy all the required data from `this.purchLine` to the `_line` object by using the setter method that was created in the `LineObject` class.</span></span>

<span data-ttu-id="b860f-179">النهج المباشر هو توسيع الأسلوبين `CopyToDocument` و`CopyToLine`.</span><span class="sxs-lookup"><span data-stu-id="b860f-179">The most straightforward approach is to extend the `CopyToDocument` and `CopyToLine` methods.</span></span> <span data-ttu-id="b860f-180">ومع ذلك، نوصي بتجريب الأسلوبين `copyToDocumentFromHeaderTable` و`copyToLineFromLineTable` أولاً.</span><span class="sxs-lookup"><span data-stu-id="b860f-180">However, we recommend that you try the `copyToDocumentFromHeaderTable` and `copyToLineFromLineTable` methods first.</span></span> <span data-ttu-id="b860f-181">إذا لم يعمل التطبيق كما هو مطلوب، فقم بتنفيذ الأسلوب الخاص بك، وقم باستدعائه في `CopyToDocument` و`CopyToLine`.</span><span class="sxs-lookup"><span data-stu-id="b860f-181">If they don't work as you require, implement your own method, and call it in `CopyToDocument` and `CopyToLine`.</span></span> <span data-ttu-id="b860f-182">هناك ثلاثه مواقف شائعه حيث يمكنك استخدام هذا الأسلوب:</span><span class="sxs-lookup"><span data-stu-id="b860f-182">There are three common situations where you might use this approach:</span></span>

- <span data-ttu-id="b860f-183">الحقل المطلوب موجود في `PurchTable` أو `PurchLine`.</span><span class="sxs-lookup"><span data-stu-id="b860f-183">The required field is in `PurchTable` or `PurchLine`.</span></span> <span data-ttu-id="b860f-184">في هذه الحالة، يمكنك توسيع `copyToDocumentFromHeaderTable` و`copyToLineFromLineTable`.</span><span class="sxs-lookup"><span data-stu-id="b860f-184">In this situation, you can extend `copyToDocumentFromHeaderTable` and `copyToLineFromLineTable`.</span></span> <span data-ttu-id="b860f-185">فيما يلي نموذج للتعليمات البرمجية.</span><span class="sxs-lookup"><span data-stu-id="b860f-185">Here is the sample code.</span></span>

    ```X++
    /// <summary>
    /// Copies to the current line of the document from.
    /// </summary>
    /// <param name = "_line">The current line of the document.</param>
    protected void copyToLineFromLineTable(TaxIntegrationLineObject _line)
    {
        next copyToLineFromLineTable(_line);
        // if we already added XXX in TaxIntegrationLineObject
        _line.setXXX(this.purchLine.XXX);
    }
    ```

- <span data-ttu-id="b860f-186">البيانات المطلوبة ليست موجودة في الجدول الافتراضي للحركة.</span><span class="sxs-lookup"><span data-stu-id="b860f-186">The required data isn't in the default table of the transaction.</span></span> <span data-ttu-id="b860f-187">ومع ذلك، توجد بعض علاقات الصلة مع الجدول الافتراضي، ويكون الحقل مطلوبا في معظم البنود.</span><span class="sxs-lookup"><span data-stu-id="b860f-187">However, there are some join relationships with the default table, and the field is required on most lines.</span></span> <span data-ttu-id="b860f-188">في هذه الحالة، قم باستبدال `getDocumentQueryObject` أو `getLineObject` للاستعلام عن الجدول بعلاقة الانضمام.</span><span class="sxs-lookup"><span data-stu-id="b860f-188">In this situation, replace `getDocumentQueryObject` or `getLineObject` to query the table by join relationship.</span></span> <span data-ttu-id="b860f-189">في المثال التالي، يتم دمج حقل **التسليم الآن** مع أمر المبيعات على مستوي البند.</span><span class="sxs-lookup"><span data-stu-id="b860f-189">In the following example, the **Deliver Now** field is integrated with the sales order at the line level.</span></span>

    ```X++
    public class TaxIntegrationSalesTableDataRetrieval
    {
        protected MCRSalesLineDropShipment mcrSalesLineDropShipment;

        /// <summary>
        /// Gets the query for the lines of the document.
        /// </summary>
        /// <returns>The query for the lines of the document</returns>
        [Replaceable]
        protected SysDaQueryObject getLineQueryObject()
        {
            return SysDaQueryObjectBuilder::from(this.salesLine)
                .where(this.salesLine, fieldStr(SalesLine, SalesId)).isEqualToLiteral(this.salesTable.SalesId)
                .outerJoin(this.mcrSalesLineDropShipment)
                .where(this.mcrSalesLineDropShipment, fieldStr(MCRSalesLineDropShipment, SalesLine)).isEqualTo(this.salesLine, fieldStr(SalesLine, RecId))
                .toSysDaQueryObject();
        }
    }
    ```

    <span data-ttu-id="b860f-190">في هذا المثال، يتم الإعلان عن المخزن المؤقت لـ `mcrSalesLineDropShipment`، ويتم تحديد الاستعلام في`getLineQueryObject`.</span><span class="sxs-lookup"><span data-stu-id="b860f-190">In this example, a `mcrSalesLineDropShipment` buffer is declared, and the query is defined in `getLineQueryObject`.</span></span> <span data-ttu-id="b860f-191">يستخدم الاستعلام العلاقة `MCRSalesLineDropShipment.SalesLine == SalesLine.RecId`.</span><span class="sxs-lookup"><span data-stu-id="b860f-191">The query uses the relationship `MCRSalesLineDropShipment.SalesLine == SalesLine.RecId`.</span></span> <span data-ttu-id="b860f-192">أثناء التوسع في هذه الحالة، يمكنك استبدال `getLineQueryObject` بكائن الاستعلام الذي قمت بإنشاءه.</span><span class="sxs-lookup"><span data-stu-id="b860f-192">While you're extending in this situation, you can replace `getLineQueryObject` with your own constructed query object.</span></span> <span data-ttu-id="b860f-193">ومع ذلك، لاحظ النقاط التالية:</span><span class="sxs-lookup"><span data-stu-id="b860f-193">However, note the following points:</span></span>

    * <span data-ttu-id="b860f-194">لأن القيمة المرجعة لأسلوب `getLineQueryObject` هي `SysDaQueryObject`، يجب عليك إنشاء هذا الكائن باستخدام نهج SysDa.</span><span class="sxs-lookup"><span data-stu-id="b860f-194">Because the return value of the `getLineQueryObject` method is `SysDaQueryObject`, you must construct this object by using the SysDa approach.</span></span>
    * <span data-ttu-id="b860f-195">لا يمكن حذف الجدول الموجود.</span><span class="sxs-lookup"><span data-stu-id="b860f-195">Can't remove existed table.</span></span>

- <span data-ttu-id="b860f-196">ترتبط البيانات المطلوبة بجدول المعاملات بعلاقة ربط معقدة، أو أن العلاقة ليست إلى واحد (1: 1) ولكنها علاقة واحدة إلى متعدد (1: N).</span><span class="sxs-lookup"><span data-stu-id="b860f-196">The required data is related to the transaction table by a complicated join relationship, or the relation isn't one to one (1:1) but one to many (1:N).</span></span> <span data-ttu-id="b860f-197">في هذه الحالة، ستصبح الأمور معقده لبعضها.</span><span class="sxs-lookup"><span data-stu-id="b860f-197">In this situation, things become a little complicated.</span></span> <span data-ttu-id="b860f-198">ينطبق هذا الموقف علي مثال الابعاد المالية.</span><span class="sxs-lookup"><span data-stu-id="b860f-198">This situation applies to the example of financial dimensions.</span></span> 

    <span data-ttu-id="b860f-199">في هذه الحالة، يمكنك تنفيذ الأسلوب الخاص بك لاسترداد البيانات.</span><span class="sxs-lookup"><span data-stu-id="b860f-199">In this situation, you can implement your own method to retrieve the data.</span></span> <span data-ttu-id="b860f-200">فيما يلي نموذج للتعليمات البرمجية في ملف `TaxIntegrationPurchTableDataRetrieval_Extension.xpp`.</span><span class="sxs-lookup"><span data-stu-id="b860f-200">Here is the sample code in the `TaxIntegrationPurchTableDataRetrieval_Extension.xpp` file.</span></span>

    ```X++
    [ExtensionOf(classStr(TaxIntegrationPurchTableDataRetrieval))]
    final class TaxIntegrationPurchTableDataRetrieval_Extension
    {
        private const str CostCenterKey = 'CostCenter';
        private const str ProjectKey = 'Project';

        /// <summary>
        /// Copies to the current line of the document from.
        /// </summary>
        /// <param name = "_line">The current line of the document.</param>
        protected void copyToLineFromLineTable(TaxIntegrationLineObject _line)
        {
            Map dimensionAttributeMap = this.getDimensionAttributeMapByDefaultDimension(this.purchline.DefaultDimension);
            if (dimensionAttributeMap.exists(CostCenterKey))
            {
                _line.setCostCenter(dimensionAttributeMap.lookup(CostCenterKey));
            }
            if (dimensionAttributeMap.exists(ProjectKey))
            {
                _line.setProjectId(dimensionAttributeMap.lookup(ProjectKey));
            }
            next copyToLineFromLineTable(_line);
        }
        private Map getDimensionAttributeMapByDefaultDimension(RefRecId _defaultDimension)
        {
            DimensionAttribute dimensionAttribute;
            DimensionAttributeValue dimensionAttributeValue;
            DimensionAttributeValueSetItem dimensionAttributeValueSetItem;
            Map ret = new Map(Types::String, Types::String);

            select Name, RecId from dimensionAttribute
                join dimensionAttributeValue
                    where dimensionAttributeValue.dimensionAttribute == dimensionAttribute.RecId
                join DimensionAttributeValueSetItem
                    where DimensionAttributeValueSetItem.DimensionAttributeValue == DimensionAttributeValue.RecId
                        && DimensionAttributeValueSetItem.DimensionAttributeValueSet == _defaultDimension;

            while(dimensionAttribute.RecId)
            {
                ret.insert(dimensionAttribute.Name, dimensionAttributeValue.DisplayValue);
                next dimensionAttribute;
            }
            return ret;
        }
    }
    ```

### <a name="step-3-add-data-to-the-request"></a><span data-ttu-id="b860f-201">الخطوة 3.</span><span class="sxs-lookup"><span data-stu-id="b860f-201">Step 3.</span></span> <span data-ttu-id="b860f-202">إضافة البيانات إلى الطلب</span><span class="sxs-lookup"><span data-stu-id="b860f-202">Add data to the request</span></span>

<span data-ttu-id="b860f-203">قم بتوسيع أسلوب `copyToTaxableDocumentHeaderWrapperFromTaxIntegrationDocumentObject` أو أسلوب `copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine` لإضافة البيانات إلى الطلب.</span><span class="sxs-lookup"><span data-stu-id="b860f-203">Extend the `copyToTaxableDocumentHeaderWrapperFromTaxIntegrationDocumentObject` or `copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine` method to add data to the request.</span></span> <span data-ttu-id="b860f-204">فيما يلي نموذج للتعليمات البرمجية في ملف `TaxIntegrationCalculationActivityOnDocument_CalculationService_Extension.xpp`.</span><span class="sxs-lookup"><span data-stu-id="b860f-204">Here is the sample code in the `TaxIntegrationCalculationActivityOnDocument_CalculationService_Extension.xpp` file.</span></span>

```X++
[ExtensionOf(classStr(TaxIntegrationCalculationActivityOnDocument_CalculationService))]
final static class TaxIntegrationCalculationActivityOnDocument_CalculationService_Extension
{
    // Define key for the form in post request
    private const str IOCostCenter = 'Cost Center';
    private const str IOProject = 'Project';

    /// <summary>
    /// Copies to <c>TaxableDocumentLineWrapper</c> from <c>TaxIntegrationLineObject</c> by line.
    /// </summary>
    /// <param name = "_destination"><c>TaxableDocumentLineWrapper</c>.</param>
    /// <param name = "_source"><c>TaxIntegrationLineObject</c>.</param>
    protected static void copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine(Microsoft.Dynamics.TaxCalculation.ApiContracts.TaxableDocumentLineWrapper _destination, TaxIntegrationLineObject _source)
    {
        next copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine(_destination, _source);
        // Set the field we need to integrated for tax service
        _destination.SetField(IOCostCenter, _source.getCostCenter());
        _destination.SetField(IOProject, _source.getProjectId());
    }
}
```

<span data-ttu-id="b860f-205">في هذا الكود، `_destination` هو كائن برنامج التضمين الذي يتم استخدامه لإنشاء طلب الترحيل، و`_source` هو كائن `TaxIntegrationLineObject`.</span><span class="sxs-lookup"><span data-stu-id="b860f-205">In this code, `_destination` is the wrapper object that is used to generate the post request, and `_source` is the `TaxIntegrationLineObject` object.</span></span> 

> [!NOTE]
> * <span data-ttu-id="b860f-206">حدد المفتاح المستخدم في نموذج الطلب كـ `private const str`.</span><span class="sxs-lookup"><span data-stu-id="b860f-206">Define the key that is used in the request form as `private const str`.</span></span>
> * <span data-ttu-id="b860f-207">قم بتعيين الحقل في أسلوب `copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine` باستخدام أسلوب `SetField`.</span><span class="sxs-lookup"><span data-stu-id="b860f-207">Set the field in the `copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine` method by using the `SetField` method.</span></span> <span data-ttu-id="b860f-208">يجب أن يكون نوع بيانات المعلمة الثانية هو `string`.</span><span class="sxs-lookup"><span data-stu-id="b860f-208">The data type of the second parameter should be `string`.</span></span> <span data-ttu-id="b860f-209">إذا لم يكن نوع البيانات هو `string`، فقم بتحويله إلى `string`.</span><span class="sxs-lookup"><span data-stu-id="b860f-209">If the data type isn't `string`, convert it to `string`.</span></span>

## <a name="appendix"></a><span data-ttu-id="b860f-210">الملحق</span><span class="sxs-lookup"><span data-stu-id="b860f-210">Appendix</span></span>

<span data-ttu-id="b860f-211">يعرض هذا الملحق رمز عينة كاملة لتكامل الأبعاد المالية (**مركز التكلفة** و **المشروع**) على مستوى البند.</span><span class="sxs-lookup"><span data-stu-id="b860f-211">This appendix shows the complete sample code for the integration of financial dimensions (**Cost center** and **Project**) at the line level.</span></span>

### <a name="taxintegrationlineobject_extensionxpp"></a><span data-ttu-id="b860f-212">TaxIntegrationLineObject_Extension.xpp</span><span class="sxs-lookup"><span data-stu-id="b860f-212">TaxIntegrationLineObject_Extension.xpp</span></span>

```X++
[ExtensionOf(classStr(TaxIntegrationLineObject))]
final class TaxIntegrationLineObject_Extension
{
    private OMOperatingUnitNumber costCenter;
    private ProjId projectId;

    /// <summary>
    /// Gets a costCenter.
    /// </summary>
    /// <returns>The cost center.</returns>
    public final OMOperatingUnitNumber getCostCenter()
    {
        return this.costCenter;
    }

    /// <summary>
    /// Sets the cost center.
    /// </summary>
    /// <param name = "_value">The cost center.</param>
    public final void setCostCenter(OMOperatingUnitNumber _value)
    {
        this.costCenter = _value;
    }

    /// <summary>
    /// Gets a project ID.
    /// </summary>
    /// <returns>The project ID.</returns>
    public final ProjId getProjectId()
    {
        return this.projectId;
    }

    /// <summary>
    /// Sets the project ID.
    /// </summary>
    /// <param name = "_value">The project ID.</param>
    public final void setProjectId(ProjId _value)
    {
        this.projectId = _value;
    }
}
```

### <a name="taxintegrationpurchtabledataretrieval_extensionxpp"></a><span data-ttu-id="b860f-213">TaxIntegrationPurchTableDataRetrieval_Extension.xpp</span><span class="sxs-lookup"><span data-stu-id="b860f-213">TaxIntegrationPurchTableDataRetrieval_Extension.xpp</span></span>

```X++
[ExtensionOf(classStr(TaxIntegrationPurchTableDataRetrieval))]
final class TaxIntegrationPurchTableDataRetrieval_Extension
{
    private const str CostCenterKey = 'CostCenter';
    private const str ProjectKey = 'Project';

    /// <summary>
    /// Copies to the current line of the document from.
    /// </summary>
    /// <param name = "_line">The current line of the document.</param>
    protected void copyToLineFromLineTable(TaxIntegrationLineObject _line)
    {
        Map dimensionAttributeMap = this.getDimensionAttributeMapByDefaultDimension(this.purchline.DefaultDimension);
        if (dimensionAttributeMap.exists(CostCenterKey))
        {
            _line.setCostCenter(dimensionAttributeMap.lookup(CostCenterKey));
        }
        if (dimensionAttributeMap.exists(ProjectKey))
        {
            _line.setProjectId(dimensionAttributeMap.lookup(ProjectKey));
        }
        next copyToLineFromLineTable(_line);
    }
    private Map getDimensionAttributeMapByDefaultDimension(RefRecId _defaultDimension)
    {
        DimensionAttribute dimensionAttribute;
        DimensionAttributeValue dimensionAttributeValue;
        DimensionAttributeValueSetItem dimensionAttributeValueSetItem;
        Map ret = new Map(Types::String, Types::String);
        select Name, RecId from dimensionAttribute
            join dimensionAttributeValue
                where dimensionAttributeValue.dimensionAttribute == dimensionAttribute.RecId
            join DimensionAttributeValueSetItem
                where DimensionAttributeValueSetItem.DimensionAttributeValue == DimensionAttributeValue.RecId
                    && DimensionAttributeValueSetItem.DimensionAttributeValueSet == _defaultDimension;
        while(dimensionAttribute.RecId)
        {
            ret.insert(dimensionAttribute.Name, dimensionAttributeValue.DisplayValue);
            next dimensionAttribute;
        }
        return ret;
    }
}
```

### <a name="taxintegrationcalculationactivityondocument_calculationservice_extensionxpp"></a><span data-ttu-id="b860f-214">TaxIntegrationCalculationActivityOnDocument_CalculationService_Extension.xpp</span><span class="sxs-lookup"><span data-stu-id="b860f-214">TaxIntegrationCalculationActivityOnDocument_CalculationService_Extension.xpp</span></span>

```X++
[ExtensionOf(classStr(TaxIntegrationCalculationActivityOnDocument_CalculationService))]
final static class TaxIntegrationCalculationActivityOnDocument_CalculationService_Extension
{
    // Define key for the form in post request
    private const str IOCostCenter = 'Cost Center';
    private const str IOProject = 'Project';

    /// <summary>
    /// Copies to <c>TaxableDocumentLineWrapper</c> from <c>TaxIntegrationLineObject</c> by line.
    /// </summary>
    /// <param name = "_destination"><c>TaxableDocumentLineWrapper</c>.</param>
    /// <param name = "_source"><c>TaxIntegrationLineObject</c>.</param>
    protected static void copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine(Microsoft.Dynamics.TaxCalculation.ApiContracts.TaxableDocumentLineWrapper _destination, TaxIntegrationLineObject _source)
    {
        next copyToTaxableDocumentLineWrapperFromTaxIntegrationLineObjectByLine(_destination, _source);
        // Set the field we need to integrated for tax service
        _destination.SetField(IOCostCenter, _source.getCostCenter());
        _destination.SetField(IOProject, _source.getProjectId());
    }
}
```
