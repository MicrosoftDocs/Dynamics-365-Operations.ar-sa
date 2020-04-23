---
title: إعادة استخدام تكوينات المنتجات
description: يمكنك تحديد إن كنت تريد إعادة استخدام تكوين موجود لمنتج تلقائيًا. بعد ذلك، عندما يكمل المستخدم جلسة العمل المخصصة للتكوين، يتحقق النظام مما إذا كان هناك أي تكوين يتطابق مع تحديدات المستخدم. إذا تم العثور على تكوين مطابق، فسيُعاد استخدام معرف التكوين وقائمة مكونات الصنف المطابقة (BOM) والمسار.
author: cvocph
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 201813
ms.assetid: 4985e308-7824-41fc-83fd-fd0bdae888e3
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9f72d93600db3d9bf0a44ac1fe84111527bb31d0
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: ar-SA
ms.lasthandoff: 04/02/2020
ms.locfileid: "3209388"
---
# <a name="reuse-product-configurations"></a><span data-ttu-id="b8b05-105">إعادة استخدام تكوينات المنتجات</span><span class="sxs-lookup"><span data-stu-id="b8b05-105">Reuse product configurations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b8b05-106">يمكنك تحديد إن كنت تريد إعادة استخدام تكوين موجود لمنتج تلقائيًا.</span><span class="sxs-lookup"><span data-stu-id="b8b05-106">You can specify that you want to automatically reuse an existing configuration for a product.</span></span> <span data-ttu-id="b8b05-107">بعد ذلك، عندما يكمل المستخدم جلسة العمل المخصصة للتكوين، يتحقق النظام مما إذا كان هناك أي تكوين يتطابق مع تحديدات المستخدم.</span><span class="sxs-lookup"><span data-stu-id="b8b05-107">Then, when a user has completed a configuration session, the system verifies whether a configuration that matches the user’s selections already exists.</span></span> <span data-ttu-id="b8b05-108">إذا تم العثور على تكوين مطابق، فسيُعاد استخدام معرف التكوين وقائمة مكونات الصنف المطابقة (BOM) والمسار.</span><span class="sxs-lookup"><span data-stu-id="b8b05-108">If a matching configuration is found, the configuration ID, corresponding bill of materials (BOM), and route are reused.</span></span>

<a name="requirements-for-reusing-configurations"></a><span data-ttu-id="b8b05-109">متطلبات إعادة استخدام التكوينات</span><span class="sxs-lookup"><span data-stu-id="b8b05-109">Requirements for reusing configurations</span></span>
---------------------------------------

<span data-ttu-id="b8b05-110">لتمكين إعادة استخدام التكوينات، يجب تحديد المعلومات التالية للمكونات والسمات في صفحة **تفاصيل نموذج تكوين المنتج‬**:</span><span class="sxs-lookup"><span data-stu-id="b8b05-110">To enable configurations to be reused, you must specify the following information for the components and attributes on the **Product configuration model details** page:</span></span>

-   <span data-ttu-id="b8b05-111">**المكونات والمكونات الفرعية** – على علامة التبويب السريعة **عام**، في الحقل **إعادة استخدام التكوينات**، حدد **نعم**.</span><span class="sxs-lookup"><span data-stu-id="b8b05-111">**Components and subcomponents** – On the **General** FastTab, in the **Reuse configurations** field, select **Yes**.</span></span>
-   <span data-ttu-id="b8b05-112">**السمات** – على علامة التبويب السريعة **السمات**، حدد الخيار **تضمين في إعادة الاستخدام‬**.</span><span class="sxs-lookup"><span data-stu-id="b8b05-112">**Attributes** – On the **Attributes** FastTab, select the **Include in reuse** option.</span></span> <span data-ttu-id="b8b05-113">يظهر هذا الخيار فقط عند تمكين المكون ذي الصلة لإعادة استخدامه.</span><span class="sxs-lookup"><span data-stu-id="b8b05-113">This option appears only when the related component is enabled for reuse.</span></span> <span data-ttu-id="b8b05-114">إذا لم تحدد أية سمات لإعادة الاستخدام، فسيُعاد استخدام التكوين دائمًا، بغض النظر عن تحديدات المستخدم أثناء جلسة العمل المخصصة للتكوين.</span><span class="sxs-lookup"><span data-stu-id="b8b05-114">If you don't select any attributes for reuse, the configuration is always reused, regardless of the user’s selections during a configuration session.</span></span> <span data-ttu-id="b8b05-115">يجب أن تتطابق قيم السمات في التكوين الموجود مع تحديدات المستخدم.</span><span class="sxs-lookup"><span data-stu-id="b8b05-115">The attribute values in the existing configuration must match the user’s selections.</span></span> <span data-ttu-id="b8b05-116">على سبيل المثال، إذا قام المستخدم بتحديد اللون **الأزرق** كلون أثناء تكوين، فإن النظام سيتحقق مما إذا كان تكوين موجود للمكون له اللون الأزرق.</span><span class="sxs-lookup"><span data-stu-id="b8b05-116">For example, if the user selects **Blue** as the color during a configuration session, the system verifies whether an existing configuration of the component has the color blue.</span></span>

## <a name="resetting-configuration-reuse"></a><span data-ttu-id="b8b05-117">إعادة تعيين إعادة استخدام التكوين</span><span class="sxs-lookup"><span data-stu-id="b8b05-117">Resetting configuration reuse</span></span>
<span data-ttu-id="b8b05-118">عند إعادة تعيين إعادة استخدام التكوين، لن تؤخذ في الاعتبار التكوينات التي تم إنشاؤها في السابق.</span><span class="sxs-lookup"><span data-stu-id="b8b05-118">When you reset configuration reuse, previously created configurations are no longer considered.</span></span> <span data-ttu-id="b8b05-119">قد تحتاج إلى إعادة تعيين إعادة استخدام التكوين إذا طرأ تغيير على قائمة مكونات الصنف أو المسار، ولكن دون أي تغيير في السمات ذات الصلة.</span><span class="sxs-lookup"><span data-stu-id="b8b05-119">You might want to reset configuration reuse if the BOM or route was changed, but no related attributes were changed.</span></span> <span data-ttu-id="b8b05-120">يمكنك إعادة تعيين إعادة استخدام التكوين على علامة التبويب السريعة **عام** للمكون.</span><span class="sxs-lookup"><span data-stu-id="b8b05-120">You reset configuration reuse on the **General** FastTab for the component.</span></span>



